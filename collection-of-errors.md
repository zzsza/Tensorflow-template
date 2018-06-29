# Collection-of-errors
- Tensorflow를 사용하면서 생겼던 Error 모음집
- Error가 발생한 상황을 자세히 작성하기
- 개인 정리 목적으로 작성하는 글이기 때문에, 다른 분들의 상황과는 다를 수 있습니다

### Estimator
- ```shuffle must be explicitly set as boolean; got None``` Error
    - ```numpy_io``` 또는 ```pandas_io```에서 발생
    - pred할 때 사용되는 함수에 shuffle 값이 True 또는 False로 들어가야 함(default는 None)

    