# 강화학습으로 공정 운전 조건 자동 제어 실습 

강화학습은 실제 상황을 environment로 정의하고, 정의한 environment에 따라 직접 episode를 만들어 학습하기 때문에 게임과 같은 상황에 많이 사용된다.

게임은 현재 상황이 성공인지 실패인지, 다음 어떤 action을 취할 수 있는지, 어떤 상황에서 어떤 action을 취하면 다음은 어떤 상황이 될 지 등 모든 environment 정의를 개발자가 직접 하면된다.
즉, simulation 할 수 있는 모든 가상의 상황을 정의할 수 있다.

한편, 화학공정과 같은 상황에서는 모든 random한 상황에 대해 결과가 어떨지 직접 실험해보는 것이 불가능에 가깝다.

따라서, 본 미니 프로젝트는 이러한 공정 운전 조건 최적화에 강화학습을 어떻게 적용하는지 알아보고자 한다. 

단, 복잡한 실제 공정이 상황이 아닌, 한개의 y값을 특정 값으로 만들기 위한 최적의 x값을 구하는 아주 간단한 예시로 진행한다. 

코드는 [Pytorch RL 튜토리얼](https://leedakyeong.tistory.com/entry/%EA%B0%95%ED%99%94%ED%95%99%EC%8A%B5-%EA%B0%95%ED%99%94%ED%95%99%EC%8A%B5%EC%9C%BC%EB%A1%9C-%EA%B3%B5%EC%A0%95-%EC%9E%90%EB%8F%99-%EC%A0%9C%EC%96%B4-%EC%8B%9C%EB%AE%AC%EB%A0%88%EC%9D%B4%EC%85%98-%ED%95%B4%EB%B3%B4%EA%B8%B0#recentEntries)을 참고하였으며, gym 게임 environment에 구현되어 있는걸 본 과정에 맞게 수정하였다. 
