# Collection-of-errors
- Tensorflow를 사용하면서 생겼던 Error 모음집
- Error가 발생한 상황과 해결하는 과정을 작성할 예정입니다
- 개인 정리 목적으로 작성하는 글이기 때문에, 다른 분들의 상황과는 다를 수 있습니다

---
## Errors
- ```shuffle must be explicitly set as boolean; got None``` Error
    - ```numpy_io``` 또는 ```pandas_io```에서 발생
    - pred할 때 사용되는 함수에 shuffle 값이 True 또는 False로 들어가야 함(default는 None)

- ```Shapes (?, 1) and (?,) are incompatible``` error
    - shape를 맞춰주기 : ```tf.expand_dims``` 사용
- ```Value passed to parameter 'x' has DataType int32 not in list of allowed values``` error
    - value의 type을 float32로 바꾸기 : ```tf.cast``` 사용
- ```Attempting to use uninitialized value accuracy/total``` error
    - accuracy는 local_variables에 속하는데, 항상 초기화를 해줘야 함
    -  ```tf.local_variables_initializer()``` 실행    