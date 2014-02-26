title:  用javascript写mangoDB脚本
date: 2014-02-26 10.10.10

MongoDB可以在shell里头执行JS， 我们可以通过写javascript让MongoDB执行一些自动化的维护任务。

以下几点需要注意：

###js用print/printjson执行打印###

    print('Hello World');
    var obj = { success： True, code: 1234 };
    printjson(obj);

##连接数据库###

    var db = connect("localhost:27017/cbf_dev");
    
##MongoDB shell加载外部文件

    >load('xxx.js')

##迭代操作doc##

    db.users.find(conditions).forEach(function (doc) {
        ....
    })

