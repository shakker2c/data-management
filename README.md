# data-management
一个简单的数据管理平台

2018/11/19 shakker2c 增加订单表格页面(OrderForm.aspx),显示订单数据。</br>
2018/11/20 shakker2c 增加订单表格页面的按钮设计。</br>
2018/11/22 shakker2c 实现按钮设计功能,数据库命令模块化。</br>
2018/11/23 shakker2c 设计数据结构保存用户的数据对象, 实现后台增删改的功能</br>
                     public struct MySqlContext {</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public MySqlConnection conn;               // 用户请求的数据库连接对象</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public MySqlCommand comm;                  // 用户请求的command命令对象</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public MySqlRequest status;                // 数据库请求的命令号</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public string context;                     // 用户请求的command命令描述</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public int res;                            // 数据库执行操作时执行的行</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public CreateCommand create_cmd;           // 用户自定义数据库命令创建方法</br>
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public CommandCallBack callback;           // 用户自定义方法</br>
                     }</br>
2018/11/24 shakker2c 设计登录页面,使用数据结构保存用户数据对象，MySqlCmd添加登录调用自定义方法防止sql注入,
                     使用Session["user_context"]保存读取数据库的内容,修改后台登录后进入订单的页面,让对应的表格显示到用户浏览器</br>
2018/11/27 shakker2c 修改自动生成mysql语句的逻辑，避免生成“”字符导致数据库中添加了无效的数据
