yamlmatlab
----------

This is a github copy of https://code.google.com/p/yamlmatlab/
that has been packaged into +yaml namespace by Yauhen Yakimovich.


Installation
------------

Just add the codes and all subfolders to Matlab path by

```matlab
addpath(genpath('path/to/codes'));
```


Usage
-----

Reading in:

```matlab
yaml_file = 'test.yaml';
YamlStruct = yaml.ReadYaml(yaml_file);
```

Writing out

 ```matlab
 x.name='Martin';
 yaml.WriteYaml('test.yaml',x)
```

Compatibility Issues
------------
R2026b and later releases: MATLAB does not include a JRE, and an OpenJDK is required to enable products and features which require Java.
To fix this issue is to do the following:
1. Install Eclipse Adoptium V25 LTS: https://adoptium.net/en-GB/temurin/releases
2. Retrieve the installation path. i.e. `C:\Program Files\Eclipse Adoptium\jdk-25.0.4.101-hotspot`
3. In MATLAB, use: `jenv("C:\Program Files\Eclipse Adoptium\jdk-25.0.4.101-hotspot")`
4. Restart MATLAB
5. In MATLAB
   ```
   jenv
   version -java
   usejave('jvm`)
   ```
Things should run smoothly after that!

Main authors
------------

* Jiri Cigler, Dept. of Control Engineering, CTU Prague http://support.dce.felk.cvut.cz/pub/ciglejir/
* Jan Siroky, Energocentrum PLUS, s.r.o.
* Pavel Tomasko, student at Faculty of Electrical Engineering, CTU Prague and Institute of Chemical Technology, Prague.
