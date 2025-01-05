
Install Java with Brew
```bash
brew install java11
```

Install Maven with Brew

```bash
brew install maven
```


Delete openjdk

```bash
brew uninstall openjdk
```

For the system Java wrappers to find this JDK, symlink it with

```bash
sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk
```

Add this to .zshrc

```bash
export JAVA_HOME=$(/usr/libexec/java_home -v 11)
export PATH="/opt/homebrew/opt/openjdk@11/bin:$PATH"
```


openjdk@11 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have openjdk@11 first in your PATH, run:

```bash
echo 'export PATH="/opt/homebrew/opt/openjdk@11/bin:$PATH"' >> ~/.zshrc
```

For compilers to find openjdk@11 you may need to set:

```bash
export CPPFLAGS="-I/opt/homebrew/opt/openjdk@11/include"
```
