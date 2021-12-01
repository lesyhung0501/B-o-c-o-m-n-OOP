# Báo cáo design partens
Báo cáo môn OOP<br>
### 1.Singleton Pattern
##### Giới thiệu về Singleton Pattern
Singleton đảm bảo chỉ duy nhất một thể hiện (instance) được tạo ra và nó sẽ cung cấp cho chúng ta một method để có thể truy xuất được thể hiện duy nhất đó mọi lúc mọi nơi trong chương trình.
##### Cách sử dụng Singleton Pattern trong link github tìm được
Trong phần repo ở [link github](https://github.com/AlexanderGrom/go-patterns) mà nhóm bọn mình đã tìm hiểu được thì việc sử dụng **Singleton Pattern** được thể hiện như sau:
```
// Package singleton is an example of the Singleton Pattern.
package singleton

import (
	"sync"
)

// Singleton implementation.
type Singleton struct {
}

var (
	instance *Singleton
	once     sync.Once
)

// GetInstance returns singleton
func GetInstance() *Singleton {
	once.Do(func() {
		instance = &Singleton{}
	})
	return instance
}
```

##### Nhận xét về cách sử dụng Singleton Pattern ở trên:
* Đoạn code cho chúng ta thấy chỉ có một instance của lớp.
* Việc quản lý việc truy cập tốt hơn vì chỉ có một thể hiện duy nhất.
* Có thể quản lý số lượng thể hiện của một lớp trong giớn hạn chỉ định.


