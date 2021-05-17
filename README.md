# os_project3_readerWriterProblem

이 프로젝트는 mutex를 사용해서 reader-writer 문제를 writer 선호 방식과 공정한 reader-writer 방식으로 해결해보면서 상호배타, 동기화에 대해 이해하는 목적의 프로젝트이다.

## Reader-Writer 문제

Reader와 writer가 공유자원에 접근할 때, reader는 다른 reader와 동시에 접근할 수 있다. 하지만 writer가 다른 writer나 reader와 동시에 접근하면 문제가 발생할 수 있는 것을 reader-writer 문제라고 한다. 이 문제를 해결하기 위한 해법에는 reader 선호, writer 선호, 공정한 reader-writer, 세 가지가 있다. 어떤 방식이든 모두 writer에게는 상호배타를 보장하고, reader에게는 다른 reader와 최대한 중복을 허용하는 것을 목표로 한다.

## Reader선호

reader가 중복해서 들어갈 수 있으며 writer보다 reader가 앞서는 방식이다.

## Writer선호

reader의 중복을 최대한 허용하되 기다리는 writer가 있으면 reader가 더 이상 writer를 앞지르지 못하게 하는 방식이다.

## 공정한 reader-writer

공정한 reader-writer는 선착순으로 CS에 들어가면서 reader의 중복을 최대한 허용하는 방식이다.

## 주요함수

pthread_mutex_lock(pthread_mutex_t *mutex) : mutex 잠금  
 pthread_mutex_unlock(pthread_mutex_t *mutex) : mutex 풂

## 느낀점

이 프로젝트를 통해 상호배타, 동기화가 실제코드에서 어떻게 구현되는지 이해할 수 있었다. 또한 reader-writer 문제를 푸는 방식에는 3가지가 있다는 것을 알게 되었고 각 3가지 방식으로 "reader와 writer의 상호배타", "reader의 중복을 허용"을 구현하는 방법을 익힐 수 있었다.
