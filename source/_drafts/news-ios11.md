---
title: DeviceCheck in iOS11
tags:
 - mobile
 - iOS
categories: 
 - Mobile
 - iOS
thumbnail:
 - http://www.startlr.com/wp-content/uploads/2017/06/apple-releases-ios-11-developer-beta-screenshot-iphone-and-ipad-pro.jpg
---

# DeviceChekck 기능이 가져올 iPhone 중고폰 시장의 파장

Apple은 사기 방지를 위한 개발측 요구와 개인 정보보호를 모두 만족시킬 수 있는 기능을 iOS 11 도입했으며, 향후 중고폰 시장에 영향을 미칠 것 같습니다.

**Device Check** 라고 하는 이 기능은, 심지어 사용자가 앱을 지웠거나 폰을 초기화(wipe)를 했다하더라도 사용자가 사용했던 특정폰을 알 수 있게 된다. Tim Cook이 Uber CEO인 Travis Kalanick이 사용자의 *지문인식* 건으로 비난했던 사건이 있었다. ([Apple CEO Time Cook spanked Uber CEO Travis Kalanick](https://www.macobserver.com/columns-opinions/editorial/time-tim-cook-spanked-uber-ceo-kalanick-breaking-rules/)) 사실 Apple도 똑같다 단지, *DeviceCheck*는 Privacy를 좀 더 고려했다고 볼 수 있다.

## *Device Check*
Device tracking이 위치 추적과는 다른 것이다. App들은 위치를 추적하기 위해서는 권한을 요청해야 하며, 사용자들은 얼마든지 권한을 바꿀 수 있다. iOS 11에서 이런 권한이 바뀌는 것은 아니다. (앞으로도 바뀌지 않는다.) DeviceCheck 기술도 지문인식을 이용한다.

iOS나 tvOS 개발자는 기기 사용자 식별을 위해 지문인식을 이용한다. DeviceCheck는 2bit와 timestamp를 이용한 태그를 디바이스를 설정한다. 이 태그는 사용자가 앱을 지우더라도 유지되지만, 개발자가 아닌 Apple에 저장된다.

더욱이, 태그는 2비트로 표현할 수 있는 4가지 형태만 있다. (00, 01, 10, 11) 
더 중요한 것은 Apple은 개발자들이 이 tag를 원하는 의미로 설정할 수 있도록 제공해 준다는 것이다.

## What This Means
Gizmodo가 밝힌 예를 보자. 개발자는 사용자가 구독을 하거나 앱을 지우기 전에 7일 동안의 평가판을 제공할 수 있다. 평가판이 시작되면, 시작의 의미로 개발사는 이 태그를 00으로 설정할 수 있다. timestamp는 시작날짜를 의미한다.

평가판 기간이 끝나고, 이용 여부 가리키는 다른 값(아마 01 정도)으로 Apple 서버에 보낼 수 있다. 그리고 timestamp는 만료 날짜를 의미한다. Katie Skinner (privacy enginner for Apple)는 다음과 같이 개발자들에게 설명했다.

<div style="text-align: right">
원문출처 : [The Mac Observer]
</div>https://www.macobserver.com/news/ios-11-devicecheck-balance-privacy-fraud-prevention-used-iphones/"