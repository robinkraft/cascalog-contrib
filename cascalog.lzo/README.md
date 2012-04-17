# Cascalog-Lzo

Based on the excellent work in Elephant-Bird:

    https://github.com/dvryaboy/elephant-bird/tree/eb-dev

## Usage

Note that this module requires Cascalog 1.9.0-wip. Add the following to `project.clj`:

    [cascalog-lzo "0.1.0-wip"]

Stay tuned for updates!

### Installing Local Dependencies

On OS X:

1. Install HomeBrew
2. brew install lzo

If you're on Lion, you'll have to re-install your java development headers [here](http://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wa/download?path=%2FDeveloper_Tools%2Fjava_for_mac_os_x_10.7_update_1_developer_package%2Fjavadeveloper_for_mac_os_x_10.7__11m3527.dmg&wosid=Mo5ndLZsjioK2DIXcKKGLmyLffK).

### Building Hadoop-Lzo

git clone https://github.com/kevinweil/hadoop-lzo.git  
cd hadoop-lzo  
git checkout -b lion 4c5a2270863e0d906e5c3c7cd7a57a7f14436759  

JAVA_HOME=$(/usr/libexec/java_home) \
C_INCLUDE_PATH=/opt/local/include LIBRARY_PATH=/opt/local/lib \
CFLAGS="-arch x86_64" ant clean compile-native test tar

### Configuring Hadoop

More information here: http://www.cloudera.com/blog/2009/11/hadoop-at-twitter-part-1-splittable-lzo-compression/


