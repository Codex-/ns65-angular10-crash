## Demo

This demo reproduces a crash when upgrading a NativeScript 6.5 App with Angular 9 to Angular 10 and running with either NS@6.8.* or NS@7.0.10

### Crashes

#### iOS

```
npm i
ns run ios
```

```
file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35: JS ERROR TypeError: Object(_nativescript_core__WEBPACK_IMPORTED_MODULE_0__["profile"]) is not a function. (In 'Object(_nativescript_core__WEBPACK_IMPORTED_MODULE_0__["profile"])(`"renderer".addScopedStyleToCss`, ɵ1$2)', 'Object(_nativescript_core__WEBPACK_IMPORTED_MODULE_0__["profile"])' is an instance of Object)
(CoreFoundation) *** Terminating app due to uncaught exception 'NativeScript encountered a fatal error: TypeError: Object(_nativescript_core__WEBPACK_IMPORTED_MODULE_0__["profile"]) is not a function. (In 'Object(_nativescript_core__WEBPACK_IMPORTED_MODULE_0__["profile"])(`"renderer".addScopedStyleToCss`, …µ1$2)', 'Object(_nativescript_core__WEBPACK_IMPORTED_MODULE_0__["profile"])' is an instance of Object)
```

#### Android

```
npm i
ns run android
```

```
System.err: An uncaught Exception occurred on "main" thread.
System.err: Unable to create application com.tns.NativeScriptApplication: com.tns.NativeScriptException: Error calling module function
System.err: TypeError: Object(...) is not a function
System.err: File: (file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35)
System.err:
System.err: StackTrace:
System.err: (file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35)
System.err:     at ../node_modules/@nativescript/angular/fesm2015/nativescript-angular.js(file:///data/data/org.nativescript.n65sample/files/app/vendor.js:95754:30)
System.err:     at __webpack_require__(file: src/webpack/bootstrap:816:0)
System.err:     at fn(file: src/webpack/bootstrap:120:0)
System.err:     at (file:///data/data/org.nativescript.n65sample/files/app/bundle.js:329:125)
System.err:     at ./main.ts(file:///data/data/org.nativescript.n65sample/files/app/bundle.js:396:30)
System.err:     at __webpack_require__(file: src/webpack/bootstrap:816:0)
System.err:     at checkDeferredModules(file: src/webpack/bootstrap:43:0)
System.err:     at webpackJsonpCallback(file: src/webpack/bootstrap:30:0)
System.err:     at (file:///data/data/org.nativescript.n65sample/files/app/bundle.js:2:57)
System.err:     at require(:1:266)
System.err:
System.err:
System.err: TypeError: Object(...) is not a function
System.err:
System.err: StackTrace:
System.err: java.lang.RuntimeException: Unable to create application com.tns.NativeScriptApplication: com.tns.NativeScriptException: Error calling module function
System.err: TypeError: Object(...) is not a function
System.err: File: (file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35)
System.err:
System.err: StackTrace:
System.err: (file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35)
System.err:     at ../node_modules/@nativescript/angular/fesm2015/nativescript-angular.js(file:///data/data/org.nativescript.n65sample/files/app/vendor.js:95754:30)
System.err:     at __webpack_require__(file: src/webpack/bootstrap:816:0)
System.err:     at fn(file: src/webpack/bootstrap:120:0)
System.err:     at (file:///data/data/org.nativescript.n65sample/files/app/bundle.js:329:125)
System.err:     at ./main.ts(file:///data/data/org.nativescript.n65sample/files/app/bundle.js:396:30)
System.err:     at __webpack_require__(file: src/webpack/bootstrap:816:0)
System.err:     at checkDeferredModules(file: src/webpack/bootstrap:43:0)
System.err:     at webpackJsonpCallback(file: src/webpack/bootstrap:30:0)
System.err:     at (file:///data/data/org.nativescript.n65sample/files/app/bundle.js:2:57)
System.err:     at require(:1:266)
System.err:
System.err:
System.err: TypeError: Object(...) is not a function
System.err:     at android.app.ActivityThread.handleBindApplication(ActivityThread.java:6465)
System.err:     at android.app.ActivityThread.access$1300(ActivityThread.java:219)
System.err:     at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1859)
System.err:     at android.os.Handler.dispatchMessage(Handler.java:107)
System.err:     at android.os.Looper.loop(Looper.java:214)
System.err:     at android.app.ActivityThread.main(ActivityThread.java:7356)
System.err:     at java.lang.reflect.Method.invoke(Native Method)
System.err:     at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492)
System.err:     at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930)
System.err: Caused by: com.tns.NativeScriptException: Error calling module function
System.err: TypeError: Object(...) is not a function
System.err: File: (file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35)
System.err:
System.err: StackTrace:
System.err: (file: node_modules/@nativescript/angular/fesm2015/nativescript-angular.js:2946:35)
System.err:     at ../node_modules/@nativescript/angular/fesm2015/nativescript-angular.js(file:///data/data/org.nativescript.n65sample/files/app/vendor.js:95754:30)
System.err:     at __webpack_require__(file: src/webpack/bootstrap:816:0)
System.err:     at fn(file: src/webpack/bootstrap:120:0)
System.err:     at (file:///data/data/org.nativescript.n65sample/files/app/bundle.js:329:125)
System.err:     at ./main.ts(file:///data/data/org.nativescript.n65sample/files/app/bundle.js:396:30)
System.err:     at __webpack_require__(file: src/webpack/bootstrap:816:0)
System.err:     at checkDeferredModules(file: src/webpack/bootstrap:43:0)
System.err:     at webpackJsonpCallback(file: src/webpack/bootstrap:30:0)
System.err:     at (file:///data/data/org.nativescript.n65sample/files/app/bundle.js:2:57)
System.err:     at require(:1:266)
System.err:
System.err:
System.err: TypeError: Object(...) is not a function
System.err:     at com.tns.Runtime.runModule(Native Method)
System.err:     at com.tns.Runtime.runModule(Runtime.java:674)
System.err:     at com.tns.Runtime.run(Runtime.java:666)
System.err:     at com.tns.NativeScriptApplication.onCreate(NativeScriptApplication.java:21)
System.err:     at android.app.Instrumentation.callApplicationOnCreate(Instrumentation.java:1182)
System.err:     at android.app.ActivityThread.handleBindApplication(ActivityThread.java:6460)
System.err:     ... 8 more
```
