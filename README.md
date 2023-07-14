# capacitor-app-update-dependency-mre

⚡️ Capacitor app to create a minimal, reproducible example. Only changes made to template were to make versions consistent with project where issue was found and add the [capacitor-rate-app](https://github.com/Nodonisko/capacitor-rate-app) plugin which has a conflicted version requirement for com.google.android.play:core.

## Steps to reproduce

1. Clone this repo
2. `npm install`
3. `cd` into `/android` directory
4. Run `./gradlew checkReleaseDuplicateClasses` or `./gradlew assembleDebug`

Expected behavior: Build succeeds

Actual behavior (full output):
```
% ./gradlew assembleDebug

> Configure project :app
WARNING: Using flatDir should be avoided because it doesn't support any meta-data formats.

> Configure project :capacitor-cordova-android-plugins
WARNING: Using flatDir should be avoided because it doesn't support any meta-data formats.

> Task :app:checkDebugDuplicateClasses FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:checkDebugDuplicateClasses'.
> A failure occurred while executing com.android.build.gradle.internal.tasks.CheckDuplicatesRunnable
   > Duplicate class com.google.android.play.core.appupdate.AppUpdateInfo found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.AppUpdateManager found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.AppUpdateManagerFactory found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.AppUpdateOptions found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.AppUpdateOptions$Builder found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.testing.FakeAppUpdateManager found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zza found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzaa found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzb found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzc found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzd found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zze found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzf found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzg found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzh found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzi found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzj found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzk found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzl found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzm found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzn found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzo found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzp found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzq found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzr found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzs found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzt found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzu found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzv found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzw found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzx found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzy found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.appupdate.zzz found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.common.IntentSenderForResultStarter found in modules core-1.10.3-runtime (com.google.android.play:core:1.10.3) and core-common-2.0.3-runtime (com.google.android.play:core-common:2.0.3)
     Duplicate class com.google.android.play.core.common.LocalTestingException found in modules core-1.10.3-runtime (com.google.android.play:core:1.10.3) and core-common-2.0.3-runtime (com.google.android.play:core-common:2.0.3)
     Duplicate class com.google.android.play.core.common.PlayCoreDialogWrapperActivity found in modules core-1.10.3-runtime (com.google.android.play:core:1.10.3) and core-common-2.0.3-runtime (com.google.android.play:core-common:2.0.3)
     Duplicate class com.google.android.play.core.install.InstallException found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.InstallState found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.InstallStateUpdatedListener found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.NativeInstallStateUpdateListener found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.model.ActivityResult found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.model.AppUpdateType found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.model.InstallErrorCode found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.model.InstallStatus found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.model.UpdateAvailability found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.model.zza found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.install.zza found in modules app-update-2.1.0-runtime (com.google.android.play:app-update:2.1.0) and core-1.10.3-runtime (com.google.android.play:core:1.10.3)
     Duplicate class com.google.android.play.core.listener.StateUpdatedListener found in modules core-1.10.3-runtime (com.google.android.play:core:1.10.3) and core-common-2.0.3-runtime (com.google.android.play:core-common:2.0.3)
     
     Go to the documentation to learn how to <a href="d.android.com/r/tools/classpath-sync-errors">Fix dependency resolution errors</a>.

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 2s
105 actionable tasks: 39 executed, 66 up-to-date
```

## Running this example

To run the provided example, you can use `npm start` command.

```bash
npm start
```
