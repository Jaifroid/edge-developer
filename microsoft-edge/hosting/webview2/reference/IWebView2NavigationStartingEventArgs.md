---
description: Host web content in your Win32 app with the Microsoft Edge WebView 2 control
title: Microsoft Edge WebView 2 for Win32 apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge
---

# interface IWebView2NavigationStartingEventArgs 

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

Event args for the NavigationStarting event.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | The uri of the requested navigation.
[get_IsUserInitiated](#get_isuserinitiated) | True when the navigation was initiated through a user gesture as opposed to programmatic navigation.
[get_IsRedirected](#get_isredirected) | True when the navigation is redirected.
[get_RequestHeaders](#get_requestheaders) | The HTTP request headers for the navigation.
[get_Cancel](#get_cancel) | The host may set this flag to cancel the navigation.
[put_Cancel](#put_cancel) | Set this flag to cancel the navigation.

## Members

#### get_Uri 

The uri of the requested navigation.

> public HRESULT [get_Uri](#interface_i_web_view2_navigation_starting_event_args_1a7baf7016c9e37181cd7caa02fc1622f3)(LPWSTR * uri)

#### get_IsUserInitiated 

True when the navigation was initiated through a user gesture as opposed to programmatic navigation.

> public HRESULT [get_IsUserInitiated](#interface_i_web_view2_navigation_starting_event_args_1a13de1f4fcca5d35871a00870c4cfa5a9)(BOOL * isUserInitiated)

#### get_IsRedirected 

True when the navigation is redirected.

> public HRESULT [get_IsRedirected](#interface_i_web_view2_navigation_starting_event_args_1a853fb130fa29cac353ec29f25b158813)(BOOL * isRedirected)

#### get_RequestHeaders 

The HTTP request headers for the navigation.

> public HRESULT [get_RequestHeaders](#interface_i_web_view2_navigation_starting_event_args_1a56153b375b49531a6f1a3f1ea04b414f)(LPWSTR * requestHeaders)

#### get_Cancel 

The host may set this flag to cancel the navigation.

> public HRESULT [get_Cancel](#interface_i_web_view2_navigation_starting_event_args_1af90cd945d26a6537306928973538b782)(BOOL * cancel)

If set, it will be as if the navigation never happened and the current page's content will be intact. For performance reasons, GET HTTP requests may happen, while the host is responding. This means cookies can be set and used part of a request for the navigation.

#### put_Cancel 

Set this flag to cancel the navigation.

> public HRESULT [put_Cancel](#interface_i_web_view2_navigation_starting_event_args_1a2e394e2be9d77286457b5889c76d27d3)(BOOL cancel)

