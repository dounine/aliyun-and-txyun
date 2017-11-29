# aliyun-and-txyun
money or speed count 

var cons = [{speed:[1,2],money:20},{speed:[2,6],money:25},{speed:[6,200],money:90}];
var fan1 = function(total,maxSpeed){
    var isSuccess = true;
    var money = 0;
    var useMaxTotal = 60*60*24*30*maxSpeed;
    for(var i in cons){
        var obj = cons[i];
        if(maxSpeed>=obj.speed[0]<=obj.speed[1]){
            if(useMaxTotal>=total){
                money = obj.money;
                break;
            }
        }
    }
    
    return money;
    
}

var fan2 = function(total,maxSpeed){
    return (Math.floor(total/1024)+1)*0.8
    
}

var tTotal = 10000;
var tSpeed = 4;
console.log(fan1(tTotal,tSpeed),fan2(tTotal,tSpeed))
