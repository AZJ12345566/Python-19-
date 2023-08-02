# Python-19-
Python学习笔记(19)
# p62 字典元素的增删改操作
scores={'张三':100,'李四':98,'王五':45}
print('张三'in scores) #True
print('张三' not in scores) #False

del scores['张三']  #输出指定的键值对
#scores.clear()  #清空字典的元素
print(scores)

scores['城六']=98  #新增元素
print(scores)

scores['城六'=100]  #修改元素
print(scores)



# p63 获取字典视图
scores={'张三':100,'李四':98,'王五':45}
#获取所有的key
keys=scores.keys()
print(keys)
print(type(keys))
print(list(keys))  #将所有key组成的视图转成列表

#获取所有的value
values=scores.values()
print(values)
print(type(values))
print(list(values))

#获取所有的key-value对
items=scores.items()
print(items)
print(list(items))  #转换之后的列表元素是由元组组成的



# 64 字典元素的遍历
scores={'张三':100,'李四':98,'王五':45}
for item in scores:
    print(item，scores[item],scores.get(item))  #这是两种获取元素的方法，scores[item]会抛异常，后者不会抛异常
