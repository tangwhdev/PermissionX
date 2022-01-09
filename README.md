# PermissionX

PermissionX 是一个用于简化Android运行时权限用法的开源库

可以使用如下的语法结构来申请运行时权限：

```kotlin
      PermissionX.request(
                this,
                android.Manifest.permission.CALL_PHONE,
                android.Manifest.permission.WRITE_EXTERNAL_STORAGE,
                android.Manifest.permission.READ_CONTACTS
            ) { allGranted, deniedList ->

                    if(allGranted){
                        call()
                    }else{
                        Toast.makeText(this,"You denied $deniedList",Toast.LENGTH_SHORT).show()
                    }

            }

```