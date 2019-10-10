---
title: "개발자 노트 4. 시장 카드"
tag:
  - "Market Card"
  - "Resource"
date: 2019-10-07 16:31
category:
  - "DevelopNote"
sidebar:
  nav: "DevelopNote"
---

## 세 번째 전략: 시장 카드 구매

Project MINE에서 점수를 얻기 위한 방법으로는 크게 세가지가 있습니다. 목표를 달성하거나, 자원을 많이 모으거나, 또는 시장 카드를 구매하는 방법이죠

이번 포스트에서는 **시장 카드**에 대해 다룹니다.

## 직접 사용할 수 있는 카드들

Project MINE은 게임을 하면서 덱을 만들어 나가고, 그 덱을 이용해서 기업을 성장시키는 게임으로 구상을 했습니다. 즉, **덱 빌딩**의 요소를 첨가한 보드게임을 만들고 싶었습니다. 도미니언과 같이 정적으로 게임을 만들 수도 있었지만, 기업이 가질 수 있는 기술은 항상 바뀌고 다양하기 때문에 오히려 어센션(Ascension) 또는 언더다크의 폭군들(Tyrant of Underdark)의 시장 보드 위에 카드를 펼치고 매 시기마다 카드가 바뀌는 시스템을 차용하였습니다.

시장 카드는 자원 카드와 계획 카드로 구성되며 이는 모두 기업이 가질 수 있는 기술들을 의미합니다. 자원 카드는 각 자원의 특색을 반영하여 자원을 쌓거나 게임을 유리하게 풀어나갈 수 있는 카드들로 구성하였고, 계획 카드는 어느 자원이 쓰던간에 윤활유로서 작용할 수 있는 카드들로 구성했습니다.

## 자원 카드: 기술의 방향

자원 카드에 5가지 특색을 부여하는 것은 어려운 일이었습니다. 서로가 확실히 달라야하고 구분이 되어야하기 때문이죠. 그러나 Project MINE에서 **점수를 얻을 수 있는 방법이 다양하고 게임이 끝나는 시점이 플레이어들의 덱에 따라 매 판마다 달라진다는 점**을 이용하여 각 자원에 다음과 같은 특색을 부여하였습니다.

### 루비

루비 자원 카드는 전반적으로 구매할 때 **비용이 저렴**합니다. 에너지 비용 역시 0 또는 1이기 때문에 **덱의 순환이 빨라 남들보다 시기를 빨리 끝낼 수 있는 장점**이 있습니다. 또한 **루비 자원도 올리기 쉽지만**, 카드의 점수가 거의 없기 때문에 루비 카드만 산다고 했을 때 **덱 점수가 낮은** 상태로 게임이 끝나는 단점이 있습니다.

### 사파이어

사파이어 자원 카드는 루비만큼은 아니지만 **구매 비용이 낮은 카드의 효율이 꽤나 높습니다**. 또한 **시장 조작과 카드 얻기, 다른 자원을 쌓기에 특성화**된 카드이기 때문에 게임 중간에 **변수**를 만드는 자원 카드 군입니다. 하지만 사파이어 자원 카드의 **구매 비용이 높은 카드들은 대부분 효율이 높지 않거나, 혼자 쓰기에도 애매하다**는 단점이 있습니다.

### 에메랄드

에메랄드 자원 카드에는 ***버려진다면 ~***과 ***제외된다면 ~*** 키워드가 있는 **유일한 자원 카드 군**입니다. 또한 카드를 **제외**하여 플레이어의 덱에서 아예 없애버려 **덱을 효율적으로 만들 수 있는 카드**가 있습니다. 각 카드의 **효과가 좋고 점수도 높기** 때문에 에메랄드 자원 카드로 덱 점수를 크게 올릴 수 있습니다. 하지만 에메랄드 자원 카드만 산다면 **사용 불가 카드**가 많아져 덱 순환이 꼬일 수 있으며, 구매 비용에 비해서 **카드의 효과가 좋은 편은 아닙니다**.

### 철

철 자원 카드는 플레이어간의 **상호작용을 중시하는 카드**들로 구성됩니다. 상대 플레이어가 **특정 행동을 했을 때 큰 이득**을 줌으로서 상대방의 플레이를 제한하는 카드가 있으며, 또는 상대 플레이어의 **손에 있는 카드를 버리게 하거나 자원을 없애는** 등 직접적으로 방해하여 상대방의 계획을 방해하는 카드들도 있습니다. 그러나 철의 카드들은 대부분 **에너지가 높기** 때문에 한 차례에 **여러 장의 카드를 쓰기 힘들고 덱 순환이 느려진다**는 단점이 있습니다.

### 금

금 자원 카드는 **크레딧을 얻거나 공용 목표를 달성하는데 치중한 카드**들로 구성됩니다. 금 자원 카드의 효과는 굉장히 강력하고 금 자원 카드가 많을 수록 효과가 더 좋아진다는 장점이 있기 때문에 금 자원을 미는 사람들을 **쉽게 견제하기 어렵습니다**. 그러나 금 자원 카드는 대체로 **구매 비용이 높고**, 다른 자원과 **섞어 쓰기 힘들다**는 단점이 있기 때문에 시장 보드 위의 카드에 영향을 많이 받습니다.

## 계획 카드: 덱을 더 잘 굴러가게

각 자원 카드는 각자마다 서로 다른 특색을 가지고 있습니다. 하지만 자원 카드만 사용한다면, 특히 두 가지 이상의 자원 카드를 섞으면 덱이 쉽게 꼬일 수 있습니다. 이런 상황을 벗어나고 **덱을 더 잘 굴러갈 수 있게 하는 카드**들을 넣었으며 구매 비용이 높은 카드들을 살 수 있도록 **크레딧을 주는 저 비용의 카드**들 또는 **전략적으로 쓸 수 있는 카드**들로 구성을 했습니다.

이번 포스트에서는 시장 카드에 대해 설명했습니다. 다음 포스트에서는 시기의 시스템과 컨셉에 대해서 설명할 예정입니다.










































































































































