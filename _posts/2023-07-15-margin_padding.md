---
layout: post
toc: true
title: "Margin, Padding 사용법"
categories: modern-javascript-deep-dive
tags: [margin, padding, TIL]
---

# Margin : (바깥쪽 여백) / Padding : (안쪽 여백)

margin 박스를 감싸는 여백!

padding은 컨텐츠를 감싸는 여백!

## 1. 방향마다 각각 지정하는 방법

- margin-top: 10px; // 위쪽

- margin-right: 20px; // 오른쪽

- margin-bottom: 15px; // 아래쪽

- margin-left: 5px; // 왼쪽

<br>

- padding-top: 10px; // 위쪽

- padding-right: 20px; // 오른쪽

- padding-bottom: 15px; // 아래쪽

- padding-left: 5px; // 왼쪽


## 2. 다 다르고 시계방향으로 작성 (상우하좌) margin/padding: 상, 우, 하, 좌)

- margin: 10px 20px 15px 5px;

<br>

- padding : 10px 20px 15px 5px;


## 3. 좌우는 같고 상하가 다를 때(margin/padding: 상, [좌=우], 하)

- margin: 5px 10px 20px;

<br>

- padding : 5px 10px 20px;

## 4. 상하 좌우 같을 때 (margin/padding:[상=하], [좌=우])

- margin 10px 20px;

<br>

- padding : 10px 20px;
