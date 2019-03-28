# map、filter等方法封装

虽然现在看不懂，但是直觉告诉我，照着打就对了，以后会懂的，小甲鱼的名言，学编程就是要不求甚解。

### map

Array.prototype._map=function(callback,context){
        var temp=[];
        for (var k = 0; k < this.length; k++) {
            temp.push(callback.call(context,this[k],k,this));
        }
        return temp;
    }

### every

Array.prototype._every=function(callback,context){
        for (var k = 0; k < this.length; k++) {
            if(!callback.call(context,this[k],k,this)){
                return false;
            }
        }
        return true;
    }

### filter

Array.prototype._filter=function(callback,context){
        var temp=[];
        for (var k = 0; k < this.length; k++) {
            callback.call(context,this[k],k,this)?temp.push(this[k]):"";
        }
        return temp;
    }

### some

Array.prototype._some=function(callback,context){
        for (var k = 0; k < this.length; k++) {
            if (callback.call(context,this[k],k,this)) {
                return true
            }
        }
        return false;
    }

