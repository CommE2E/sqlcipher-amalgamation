# SQLCipher amalgamation file for React Native

[![npm version](https://badge.fury.io/js/sqlcipher-amalgamation.svg)](https://badge.fury.io/js/sqlcipher-amalgamation)

SQLCipher C sources amalgamation file NPM package for building in the React Native project.

## Using for Android builds

You can use it as an npm package dependency at the top level of the project and include it in the `native/android/app/CMakeLists.txt`:

```
include_directories(
	...
	../../node_modules/@commapp/sqlcipher-amalgamation/src
)

file(GLOB SQLCIPHER "../../node_modules/@commapp/sqlcipher-amalgamation/src/*.c")

add_library(
	...
	${SQLCIPHER}
)
```

## Using for iOS

The package must be installed as an npm dependency at the top level of the project and include in the `native/ios/Podfile`:

```
target 'Project' do
	...
	pod 'SQLCipher-Amalgamation', :path => '../../node_modules/@commapp/sqlcipher-amalgamation'
```

## Release and versioning

This package release version is the same as the SQLCipher release version.