AndroidInstrumentationTests
===========================
1. Directory with tests:
app/src/tests

2. How to set test folder?
- In build.gradle file in section android mark source, f.i:

android {
        sourceSets {
            main {
                manifest.srcFile 'src/main/AndroidManifest.xml'
                java.srcDirs = ['src/main/java']
                resources.srcDirs = ['src/main/java']
                renderscript.srcDirs = ['src/main/java']
                res.srcDirs = ['src/main/res']
                assets.srcDirs = ['assets']
            }
            androidTest.setRoot('src/tests')
            androidTest.java.srcDirs = ['src/tests/src']
        }
  }
  
- Create folder following the marked route.
Result: "src" folder in "tests" should be coloured in green and to be runnable.
