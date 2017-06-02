A simple Library made to make the process of executing command lines through java programs simpler. It also returns the output line by line.  

The following snippets show how to execute a command, e.g, "adb devices -l", and redirect the output to the console:

```java
new Executer(new ExecuterStreamFormatter())  
.execute(new CommandBuilder()  
.forCommandLine("adb devices")  
.withOptions(new String[]{"-l"})  
.build());  
}catch(IOException e){
e.printStackTrace();
}
```

  Say You want to redirect the output to another object, e.g, a JTextArea named outputArea, You only have to modify the first line:  
First, outputArea must implement the Appender interface provided in the library.  
Now, You can pass it to the ExecuterStreamFormatter instance:  

```java
new ExecuterStreamFormatter(outputArea); 
```

  This library is the base of (Simple-ADB) program found here :
[xda-developers](http://forum.xda-developers.com/android/software/revive-simple-adb-tool-t3417155) , [Source-Forge](https://sourceforge.net/projects/sadb/) , [GitHub](https://github.com/mhashim6/Simple-ADB)..
