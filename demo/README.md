# demo
## 1

```
import 'package:flutter/material.dart';
import 'package:flutter/services.dart';
import 'package:flutter_svg/flutter_svg.dart';

void main() {
  runApp(const NiLuoPage());
}

class NiLuoPage extends StatelessWidget {
  const NiLuoPage({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {


    // 获取屏幕宽高
    double screenWidth = MediaQuery.of(context).size.width;
    double screenHeight = MediaQuery.of(context).size.height;
    return MaterialApp(
      // Root widget
        home: Scaffold(
            appBar: AppBar(
              title: const Text("小尼诺"),
              centerTitle: true, // 是文字居中显示
            ),
            body:
            Stack(
              children: [
                SingleChildScrollView(
                    child: Padding(
                      padding: EdgeInsets.all(20.0),
                      child: Column(
                        children: [
                          //身体上面部分
                          Column(
                              crossAxisAlignment: CrossAxisAlignment.stretch,
                              // 让所有子组件横向填满父容器
                              children: [
                                Padding(
                                  //外层加一个padding，目的是给每个 Container 添加了左右和上下的间距，确保它们不撑满整个屏幕宽度，同时也不影响容器内的子组件排版。
                                  padding:
                                  EdgeInsets.symmetric(horizontal: 20.0, vertical: 10.0),
                                  child: Container(
                                    //为第一个整体加入一个，从而增加外边框颜色
                                    decoration: BoxDecoration(
                                        border: Border.all(
                                          color: Colors.grey, //加边框颜色
                                          width: 1.0,
                                        )),
                                    //padding: ,
                                    child: Column(
                                      //整体的第一个
                                      crossAxisAlignment: CrossAxisAlignment.start, // 左对齐
                                      children: [
                                        Container(
                                          padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                          child: Text(
                                            "安全统筹",
                                            style: TextStyle(
                                                fontSize: 16, fontWeight: FontWeight.bold),
                                            //textAlign: TextAlign.left,
                                          ),
                                        ),
                                        SizedBox(height: 20),
                                        SingleChildScrollView(
                                          scrollDirection: Axis.horizontal, // 允许横向滚动
                                          child:  Wrap(children: [
                                            Flexible(
                                              flex: 1,
                                              child:  Container(
                                                // 第一个图标
                                                color: Colors.red,
                                                width: 50, // 设置宽度
                                                height: 50, // 设置高度
                                                margin: EdgeInsets.only(
                                                    left: 16.0), // 给第一个图标加和左边的间距
                                              ),
                                            ),
                                            SizedBox(width: 300), // 控制图标之间的间距
                                            Flexible(
                                              flex: 1,
                                              child: Container(
                                                color: Colors.orange,
                                                width: 50,
                                                height: 50,
                                              ),
                                            ),
                                            SizedBox(width: 300),
                                            Flexible(
                                              flex: 1,
                                              child: Container(
                                                color: Colors.green,
                                                width: 50,
                                                height: 50,
                                              ),
                                            ),
                                            SizedBox(width: 200),
                                            Flexible(
                                              flex: 1,
                                              child:  Container(
                                                color: Colors.yellow,
                                                width: 50,
                                                height: 50,
                                              ),
                                            )
                                          ]),
                                        )
                                      ],
                                    ),
                                  ),
                                ),
                                SizedBox(height: 50.0),
                                Padding(
                                  padding:
                                  EdgeInsets.symmetric(horizontal: 20.0, vertical: 10.0),
                                  child: Container(
                                    //为第二个个整体加入一个，从而增加外边框颜色

                                    decoration: BoxDecoration(
                                        border: Border.all(
                                          color: Colors.grey, //加边框颜色
                                          width: 1.0,
                                        )),
                                    //padding: ,
                                    child: Column(
                                      //整体的第二个
                                      crossAxisAlignment: CrossAxisAlignment.start,
                                      // 使这个column下的子组件左对齐
                                      children: [
                                        Container(
                                          padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                          child: Text(
                                            "我的服务",
                                            style: TextStyle(
                                                fontSize: 16, fontWeight: FontWeight.bold),
                                            //textAlign: TextAlign.left,
                                          ),
                                        ),
                                        SizedBox(height: 20),
                                        SingleChildScrollView(
                                          scrollDirection: Axis.horizontal,

                                          child:Wrap( children: [
                                            Container(
                                              // 第一个图标
                                              color: Colors.red,
                                              width: 50, // 设置宽度
                                              height: 50, // 设置高度
                                              margin: EdgeInsets.only(
                                                  left: 16.0), // 给第一个图标加和左边的间距
                                            ),
                                            SizedBox(width: 300), // 控制图标之间的间距
                                            Container(
                                              color: Colors.orange,
                                              width: 50,
                                              height: 50,
                                            ),
                                            SizedBox(width: 300),
                                            Container(
                                              color: Colors.green,
                                              width: 50,
                                              height: 50,
                                            ),
                                            SizedBox(width: 200),
                                            Container(
                                              color: Colors.yellow,
                                              width: 50,
                                              height: 50,
                                            ),
                                          ]),
                                        ),
                                        SizedBox(height: 20),
                                        SingleChildScrollView(
                                          scrollDirection: Axis.horizontal,

                                          child:Wrap(  children: [
                                            Container(
                                              // 第一个图标
                                              color: Colors.red,
                                              width: 50, // 设置宽度
                                              height: 50, // 设置高度
                                              margin: EdgeInsets.only(
                                                  left: 16.0), // 给第一个图标加和左边的间距
                                            ),
                                            SizedBox(width: 300), // 控制图标之间的间距
                                            Container(
                                              color: Colors.orange,
                                              width: 50,
                                              height: 50,
                                            ),
                                          ]),
                                        )
                                      ],
                                    ),
                                  ),
                                ),
                                SizedBox(height: 50.0),
                                Padding(
                                  padding:
                                  EdgeInsets.symmetric(horizontal: 20.0, vertical: 10.0),
                                  child: Container(
                                    //为第三个整体加入一个，从而增加外边框颜色

                                    //给每个 Container 添加了左右和上下的间距，确保它们不撑满整个屏幕宽度，同时也不影响容器内的子组件排版。
                                    decoration: BoxDecoration(
                                        border: Border.all(
                                          color: Colors.grey, //加边框颜色
                                          width: 1.0,
                                        )),
                                    width: double.infinity,
                                    // 设置宽度为 infinity，使其左右宽度撑满最外面这一层的 Column
                                    //padding: ,
                                    child: SingleChildScrollView(
                                      scrollDirection: Axis.horizontal,
                                      child: Column(
                                        //整体的第三个
                                        crossAxisAlignment: CrossAxisAlignment.start,
                                        // 左对齐

                                        children: [
                                          Container(
                                            padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                            child: Text(
                                              "推荐服务",
                                              style: TextStyle(
                                                  fontSize: 15, fontWeight: FontWeight.bold),
                                              //textAlign: TextAlign.left,
                                            ),
                                          ),
                                          SizedBox(height: 15),
                                          Container(
                                            padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                            child: Text(
                                              "查知实验室",
                                              style: TextStyle(
                                                  fontSize: 20, fontWeight: FontWeight.bold),
                                              //textAlign: TextAlign.left,
                                            ),
                                          ),
                                          SizedBox(height: 15),
                                          Container(
                                            padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                            child: Text(
                                              "合作专区",
                                              style: TextStyle(
                                                  fontSize: 16, fontWeight: FontWeight.bold),
                                              //textAlign: TextAlign.left,
                                            ),
                                          ),
                                          SizedBox(height: 15),
                                          Container(
                                            padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                            child: Text(
                                              "帮助与反馈",
                                              style: TextStyle(
                                                  fontSize: 20, fontWeight: FontWeight.bold),
                                              //textAlign: TextAlign.left,
                                            ),
                                          ),
                                          SizedBox(height: 15),
                                          Container(
                                            padding: EdgeInsets.all(8.0), // 可以为文本添加一些边距
                                            child: Text(
                                              "退出登录",
                                              style: TextStyle(
                                                  fontSize: 16, fontWeight: FontWeight.bold),
                                              //textAlign: TextAlign.left,
                                            ),
                                          ),
                                        ],
                                      ),
                                    ),
                                  ),
                                ),
                                // 使用Expanded来让容器占满可用空间，并保留底部空白
                              ]),
                          // 底部导航栏
                          Align(
                            alignment: Alignment.bottomCenter,// Align 到底部
                            child: Padding(
                              padding:
                              EdgeInsets.symmetric(horizontal: 20.0, vertical: 10.0),
                              child:  Container(
                                  width: screenWidth, // 设置容器宽度为屏幕宽度
                                  height: screenHeight * 0.2, // 设置容器高度为屏幕高度的 10%
                                  decoration: BoxDecoration(
                                      border: Border.all(
                                        color: Colors.grey, //加边框颜色
                                        width: 1.0,
                                      )),
                                  child:
                                  SingleChildScrollView(
                                    scrollDirection: Axis.horizontal, // 水平滑动

                                    child: Wrap(children: [
                                      Container(
                                        // 第一个图标
                                        color: Colors.red,
                                        width: 50, // 设置宽度
                                        height: 50, // 设置高度
                                        margin:
                                        EdgeInsets.only(left: 300.0), // 给第一个图标加和左边的间距
                                      ),
                                      SizedBox(width: 300), // 控制图标之间的间距
                                      Container(
                                        color: Colors.orange,
                                        width: 50,
                                        height: 50,
                                        margin:
                                        EdgeInsets.only(right: 300.0),
                                      ),
                                    ]),
                                  )
                              ),
                            ) ,
                          )

                        ],
                      ),
                    )),
              ],
            )

        ));
  }
}
```