# 보다 현실적인 세상

이번 수업에서 다룬 환경에서 Peter(피터)는 피로나 배고픔을 거의 느끼지 않으며 돌아다닐 수 있었습니다. 보다 현실적인 세상에서 피터는 가끔씩 앉아서 휴식도 취해야 하고 음식도 먹어야 합니다. 다음 규칙을 적용해 세상을 좀 더 현실감 있게 만들어 봅시다:

1. 한 장소에서 다른 장소로 이동함으로써 피터는 **에너지**를 잃고 약간의 **피로**를 얻습니다.
2. 피너는 사과를 먹음으로써 더 많은 에너지를 얻을 수 있습니다.
3. 피터는 나무 아래나 잔디밭에 쉬면서 (즉, 나무나 풀이 있는 보드 위의 칸(녹색 들판) 안으로 걸어 들어감으로써) 피로를 없앨 수 있습니다.
4. 피터는 늑대를 찾아 죽여야 합니다.
5. 늑대를 죽이기 위해 피터는 일정 수준의 에너지와 피로도가 필요합니다. 그렇지 않으면 늑대와의 전투에서 집니다.

## 설명

원본 Jupyter Notebook(노트북)인 [notebook.ipynb](notebook.ipynb)을 이 과제의 솔루션(해법)의 시작점으로 사용하면 됩니다.

게임의 규칙에 따라 보상 함수를 수정하고, 강화학습 알고리즘을 실행해 게임에서 승리하기 위한 최선의 행동 전략을 학습하도록 해 보세요. 그런 다음 게임에서 승리 및 패배한 횟수를 기준으로 본인의 알고리즘 성적을 무작위 걷기의 성적과 비교해 보세요.

> **참고**: 새로운 세계에서는 state(상황)이 더 복잡하며, 사람의 위치뿐만 아니라 피로도와 에너지도 필요합니다. 상황을 `(Board(보드), energy(에너지), fatigue(피로))`와 같이 tuple(튜플)로 표현해도 되고, 상황을 위해 새 class(클래스)를 (`Board` 클래스에서 파생해) 정의하거나, 또는 [rlboard.py](rlboard.py)에 이미 정의된 `Board` 클래스를 알맞게 수정하여 사용해도 됩니다.

본인의 해법에 무작위 걷기 전략에 해당하는 코드를 반드시 그대로 남겨 두고, 마지막에 본인의 알고리즘과 무작위 걷기의 성적을 비교해 보시기 바랍니다.

> **참고**: 새로운 해법이 제대로 작동하게 하기 위해서는 hyperparameter(초매개변수), 특히 epoch(에포크) 수를 조정해야 할 수도 있습니다. 게임(늑대와의 전투)에서 승리하는 것은 드문 일이기 때문에 훨씬 더 긴 학습 시간이 필요할 겁니다.

## 평가기준표

| 평가기준 | 모범                                                                                                                                        |적절                                                                                                                                    | 향상 필요                                                                                         |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------- |--------------------------------------------------------------------------------------------------------------------------------------- |------------------------------------------------------------------------------------------------ |
|          | 새로운 게임 규칙, Q-learning(Q 러닝) 알고리즘, 설명 글을 노트북에 포함하여 제시함. 제시된 Q 러닝으로 무작위 걷기에 비해 성적을 크게 향상시킬 수 있음. | 노트북에 제시된 Q 러닝이 무작위 걷기에 비해 성적을 더 향상시키기는 하지만 그 정도가 작음. 또는 노트북에 설명이 부족하고 코드가 잘 구조화되지 않음. | 게임 규칙을 재정의해 적용하려 했으나 Q 러닝 알고리즘이 작동하지 않거나 보상 함수가 완전히 정의되지 않음. |