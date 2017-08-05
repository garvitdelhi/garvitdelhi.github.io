---
layout: post
title:  "SoK Journey So Far"
date:   2014-12-21 14:34:25
categories: KDE SOK
tags: KDE
---
This month so far was full of shocking news. My mentor Anuj pahuja informed me that someone has already ported app kturtle which i had to port during the SoK duration. He said that this work was done when i was busy in my annual examination. But i thank alot to my mentor that he stood with me and helped me get another app so that i can port it. So now i am working on porting app KNetWalk that belong to Kde Games.

So far i have ported the build system and it has already bean pushed to the frameworks branch of KNetWalk. You can have a look at my progress at [quickgit](http://quickgit.kde.org/?p=knetwalk.git) on frameworks branch.

App is able to build and install successfully on kf5 on my local system. I will push other changes soon.

Now I am looking forward to port ui as now app is crashing because ui is not ported.

Cmake Log:

{% highlight bash %}
garvit@beast:~/dev/sok/knetwalk/build$ cmake ../
-- The C compiler identification is GNU 4.9.1
-- The CXX compiler identification is GNU 4.9.1
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Found KF5CoreAddons: /usr/lib/x86_64-linux-gnu/cmake/KF5CoreAddons/KF5CoreAddonsConfig.cmake (found version "5.3.0")
-- Found KF5Config: /usr/lib/x86_64-linux-gnu/cmake/KF5Config/KF5ConfigConfig.cmake (found version "5.3.0")
-- Found KF5ItemModels: /usr/lib/x86_64-linux-gnu/cmake/KF5ItemModels/KF5ItemModelsConfig.cmake (found version "5.3.0")
-- Found KF5WidgetsAddons: /usr/lib/x86_64-linux-gnu/cmake/KF5WidgetsAddons/KF5WidgetsAddonsConfig.cmake (found version "5.3.0")
-- Found KF5WindowSystem: /usr/lib/x86_64-linux-gnu/cmake/KF5WindowSystem/KF5WindowSystemConfig.cmake (found version "5.3.0")
-- Found KF5Codecs: /usr/lib/x86_64-linux-gnu/cmake/KF5Codecs/KF5CodecsConfig.cmake (found version "5.3.0")
-- Found KF5Archive: /usr/lib/x86_64-linux-gnu/cmake/KF5Archive/KF5ArchiveConfig.cmake (found version "5.3.0")
-- Found KF5DBusAddons: /usr/lib/x86_64-linux-gnu/cmake/KF5DBusAddons/KF5DBusAddonsConfig.cmake (found version "5.3.0")
-- Found KF5DNSSD: /usr/lib/x86_64-linux-gnu/cmake/KF5DNSSD/KF5DNSSDConfig.cmake (found version "5.3.0")
-- Found Gettext: /usr/bin/msgmerge (found version "0.19.2")
-- Found PythonInterp: /usr/bin/python (found version "2.7.8")
-- Found KF5Declarative: /usr/lib/x86_64-linux-gnu/cmake/KF5Declarative/KF5DeclarativeConfig.cmake (found version "5.3.0")
-- Found KF5I18n: /usr/lib/x86_64-linux-gnu/cmake/KF5I18n/KF5I18nConfig.cmake (found version "5.3.0")
-- Found KF5GuiAddons: /usr/lib/x86_64-linux-gnu/cmake/KF5GuiAddons/KF5GuiAddonsConfig.cmake (found version "5.3.0")
-- Found KF5Service: /usr/lib/x86_64-linux-gnu/cmake/KF5Service/KF5ServiceConfig.cmake (found version "5.3.0")
-- Found KF5ConfigWidgets: /usr/lib/x86_64-linux-gnu/cmake/KF5ConfigWidgets/KF5ConfigWidgetsConfig.cmake (found version "5.3.0")
-- Found KF5ItemViews: /usr/lib/x86_64-linux-gnu/cmake/KF5ItemViews/KF5ItemViewsConfig.cmake (found version "5.3.0")
-- Found KF5IconThemes: /usr/lib/x86_64-linux-gnu/cmake/KF5IconThemes/KF5IconThemesConfig.cmake (found version "5.3.0")
-- Found KF5Completion: /usr/lib/x86_64-linux-gnu/cmake/KF5Completion/KF5CompletionConfig.cmake (found version "5.3.0")
-- Found KF5JobWidgets: /usr/lib/x86_64-linux-gnu/cmake/KF5JobWidgets/KF5JobWidgetsConfig.cmake (found version "5.3.0")
-- Found KF5TextWidgets: /usr/lib/x86_64-linux-gnu/cmake/KF5TextWidgets/KF5TextWidgetsConfig.cmake (found version "5.3.0")
-- Found KF5GlobalAccel: /usr/lib/x86_64-linux-gnu/cmake/KF5GlobalAccel/KF5GlobalAccelConfig.cmake (found version "5.3.0")
-- Found KF5XmlGui: /usr/lib/x86_64-linux-gnu/cmake/KF5XmlGui/KF5XmlGuiConfig.cmake (found version "5.3.0")
-- Found KF5Crash: /usr/lib/x86_64-linux-gnu/cmake/KF5Crash/KF5CrashConfig.cmake (found version "5.3.0")
-- Found KF5Bookmarks: /usr/lib/x86_64-linux-gnu/cmake/KF5Bookmarks/KF5BookmarksConfig.cmake (found version "5.3.0")
-- Found KF5KIO: /usr/lib/x86_64-linux-gnu/cmake/KF5KIO/KF5KIOConfig.cmake (found version "5.3.0")
-- Found KF5NotifyConfig: /usr/lib/x86_64-linux-gnu/cmake/KF5NotifyConfig/KF5NotifyConfigConfig.cmake (found version "5.3.0")
-- Found KF5NewStuff: /usr/lib/x86_64-linux-gnu/cmake/KF5NewStuff/KF5NewStuffConfig.cmake (found version "5.3.0")
-- Found KF5KDELibs4Support: /usr/lib/x86_64-linux-gnu/cmake/KF5KDELibs4Support/KF5KDELibs4SupportConfig.cmake (found version "5.3.0")
-- Found KF5: success (found version "5.3.0") found components:  CoreAddons Config ItemModels WidgetsAddons WindowSystem Codecs Archive Config DBusAddons DNSSD Declarative I18n GuiAddons Service ConfigWidgets ItemViews IconThemes Completion JobWidgets TextWidgets GlobalAccel XmlGui Crash Bookmarks KIO NotifyConfig NewStuff KDELibs4Support
-- Looking for __GLIBC__
-- Looking for __GLIBC__ - found
-- Performing Test _OFFT_IS_64BIT
-- Performing Test _OFFT_IS_64BIT - Success
-- Configuring done
-- Generating done
-- Build files have been written to: /home/garvit/dev/sok/knetwalk/build
{% endhighlight %}

Make Log can be find here at this [gist](https://gist.github.com/garvitdelhi/0e21a095dcfc8cfef170)
