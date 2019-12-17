all: strings strings_arm64 slices slices_arm64 structs structs_arm64 functions functions_arm64

slices: slices.go
	GOOS=linux go build -gcflags '-N -l' slices.go

slices_arm64: slices.go
	CC=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang CXX=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang++ CGO_ENABLED=1 GOOS=android GOARCH=arm64 go build -o slices_arm64 -gcflags '-N -l' slices.go

strings: strings.go
	GOOS=linux go build -gcflags '-N -l' strings.go

strings_arm64: strings.go
	CC=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang CXX=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang++ CGO_ENABLED=1 GOOS=android GOARCH=arm64 go build -o strings_arm64 -gcflags '-N -l' strings.go

structs: structs.go
	GOOS=linux go build -gcflags '-N -l' structs.go

structs_arm64: structs.go
	CC=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang CXX=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang++ CGO_ENABLED=1 GOOS=android GOARCH=arm64 go build -o structs_arm64 -gcflags '-N -l' structs.go


functions: functions.go
	GOOS=linux go build -gcflags '-N -l' functions.go

functions_arm64: functions.go
	CC=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang CXX=/media/storage/android/ndk32/bin/aarch64-linux-android21-clang++ CGO_ENABLED=1 GOOS=android GOARCH=arm64 go build -o functions_arm64 -gcflags '-N -l' functions.go

clean:
	rm functions structs strings slices
	rm functions_arm64 structs_arm64 strings_arm64 slices_arm64
