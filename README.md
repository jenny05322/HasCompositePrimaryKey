# Laravel Model 多主鍵時的調整方式
## 使用
1. use 載入程式
2. primaryKey 用陣列的方式寫入
3. incrementing 設成 false
## 範例
```
<?php

namespace App;

use Illuminate\Database\Eloquent\Model;
use Sunnet\Core\App\HasCompositePrimaryKey;

class ModelName extends Model
{
    use HasCompositePrimaryKey;

    protected $primaryKey = ['key1', 'key2'];
    public $incrementing = false;
}
```
