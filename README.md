Wellcome,

This is a repository for the project Arieslinter.

First, you need to install the Arieslinter in your local maven repository:
```
git clone https://github.com/viRafael/arieslinter.git

cd arieslinter

mvn clean install
```
---

add file checkstyle.xml in your project root directory.

---

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE module PUBLIC "-//Puppy Crawl//DTD Check Configuration 1.3//EN"
        "http://checkstyle.sourceforge.net/dtds/configuration_1_3.dtd">

<module name="Checker">
    <module name="TreeWalker">
        <module name="br.ufba.arieslinter.checks.ConditionalTestLogicCheck"/>
        <module name="br.ufba.arieslinter.checks.DefaultTestCheck"/>
        <module name="br.ufba.arieslinter.checks.ExceptionHandlingCheck"/>
        <module name="br.ufba.arieslinter.checks.IgnoredTestCheck"/>
        <module name="br.ufba.arieslinter.checks.MagicNumberCheck"/>
        <module name="br.ufba.arieslinter.checks.RedundantPrintCheck"/>
        <module name="br.ufba.arieslinter.checks.SensitiveEqualityCheck"/>
        <module name="br.ufba.arieslinter.checks.SleepyTestCheck"/>
        <module name="br.ufba.arieslinter.checks.UnkwonFixtureCheck"/>
        <module name="br.ufba.arieslinter.checks.VerboseTestCheck"/>
    </module>
</module>
```


---

## For Visual Studio Code

Add the VSCode plugin "Checkstyle for Java"

add in your settings.xml - VSCODE

```
"java.checkstyle.configuration": "${workspaceFolder}/checkstyle.xml",
"java.checkstyle.autocheck": true,
"java.checkstyle.modules": ["/home/{user}/.m2/repository/br/ufba/arieslinter/1.0/arieslinter-1.0.jar"],
```

replace the "{user}" with your user name in your system. Ex. /home/rafael/

---
## For IntelliJ

Add the plugin "CheckStyle-IDEA" in your Intellij.
https://plugins.jetbrains.com/plugin/1065-checkstyle-idea

In the windows settings:
Settings -> Tools -> Checkstyle

in "Configuration File" add "+":
- Description: Arieslinter
- User a local Checkstyle file: your_path_checkstyle.xml
- Scan Scope: All files in project

in "Third-Party Checks" add "+":
- path: you_path_for_arieslinter-1.0.jar       ex: /home/user/.m2/repository/br/ufba/arieslinter/1.0/arieslinter-1.0.jar




