__file__
这个变量的值等于当前文件所在的路径

pycharm 错误记录:
 from twisted.scripts import trial
ModuleNotFoundError: No module named 'twisted'

修改 *.iml文件
  将:
  <component name="TestRunnerService">
    <option name="projectConfiguration" value="Twisted Trial" />
    <option name="PROJECT_TEST_RUNNER" value="Twisted Trial" />
  </component>
  修改为:
  <component name="TestRunnerService">
    <option name="PROJECT_TEST_RUNNER" value="Unittests" />
  </component>
  
  
2018-5-22 21:17:53
python学习 http://docs.python-guide.org/en/latest/

把字符串变成变量名:  locals()['age'] = 18   print(age)  输出18

python:
      if x in lst_1 or x in lst_2: print(x)
==>   if x in lst_1 + lst_2: print(x)

list内置sort方法支持定制排序
list.sort(key=lambda x: x.name)

组合公式推导, 链接 https://wenku.baidu.com/view/9897a2348bd63186bdebbc41.html

f = open(path)
json.dumps(dic, f, ensure_ascii=False)   # 有中文存入文件,  加参数ensure_ascii=False, 关闭映射ascii
f.close()

json.dump(src, f)  存文件  ret = json.dumps(src) 返回结果

[列表深浅复制](https://www.cnblogs.com/blaomao/p/7239203.html)

pycharm会自动把当前项目路径添加到sys.path,
所以部署的代码会有个定式写法:
import os, sys
sys.path.append(os.path.dirname(os.getcwd()))

2018-7-12 20:08:01
今天断线重连出bug调很久, 玩家连接时我发了断线重连协议, 玩家一重连就发送进入房间协议
