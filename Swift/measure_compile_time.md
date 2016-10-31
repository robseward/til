Measure compile time
======

Add these flags to `Other Swift Flags` in project build settings:  -Xfrontend -debug-time-function-bodies.

Run this in the console:

xcodebuild -workspace App.xcworkspace -scheme App clean build | grep [1-9].[0-9]ms | sort -nr > culprits.txt

This will output lines that take the longest to compile first.

More detail here:
http://irace.me/swift-profiling
