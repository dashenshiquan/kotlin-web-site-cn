---
type: doc
layout: reference
title: "Kotlin 多平台"
---

# Kotlin 多平台

> 多平台项目处于 [Alpha](evolution/components-stability.html) 版。语言特性与工具都可能在未来的 Kotlin 版本中发生变化。
{:.note}

Support for multiplatform programming is one of Kotlin’s key benefits. It reduces time spent writing and maintaining the
 same code for [different platforms](mpp-supported-platforms.html) while retaining the flexibility and benefits of native programming. 
 Learn more about [Kotlin Mutliplatform benefits](multiplatform.html).

With Kotlin Multiplatform, share the code using the mechanisms Kotlin provides: 
 
*   [Share code among all platforms used in your project](mpp-share-on-platforms.html#share-code-on-all-platforms). Use it for sharing the common 
business logic that applies to all platforms. 
     
    ![Code shared for all platforms]({{ url_for('asset', path='images/reference/mpp/flat-structure.png') }})
    
*   [Share code among some platforms](mpp-share-on-platforms.html#share-code-on-similar-platforms) included in your project but not all. You can 
reuse much of the code in similar platforms using a hierarchical structure. You can use [target shortcuts](mpp-share-on-platforms.html#use-target-shortcuts) 
for common combinations of targets or [create the hierarchical structure manually](mpp-share-on-platforms.html#configure-the-hierarchical-structure-manually).
    
    <img class="img-responsive" src="{{ url_for('asset', path='images/reference/mpp/iosmain-hierarchy.png') }}" alt="Code shared for iOS targets" width="400"/>

    ![Hierarchical structure]({{ url_for('asset', path='images/reference/mpp/hierarchical-structure.png') }})

If you need to access platform-specific APIs from the shared code, use the Kotlin mechanism of [expected and actual 
declarations](mpp-connect-to-apis.html).

## 教程

* [Creating a multiplatform Kotlin library](/docs/tutorials/mpp/multiplatform-library.html) teaches how to create a multiplatform 
library available for JVM, JS, and Native and which can be used from any other common code (for example, shared with 
Android and iOS). It also shows how to write tests which will be executed on all platforms and use an efficient implementation
 provided by a specific platform.
 
* [Building a Full Stack Web App with Kotlin Multiplatform](https://play.kotlinlang.org/hands-on/Full%20Stack%20Web%20App%20with%20Kotlin%20Multiplatform/01_Introduction) 
  teaches the concepts behind building an application that targets Kotlin/JVM and Kotlin/JS by building a client-server 
  application that makes use of shared code, serialization, and other multiplatform paradigms. It also provides a brief
  introduction to working with Ktor both as a server- and client-side framework.
