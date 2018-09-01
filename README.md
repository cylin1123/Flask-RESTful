# Flask-RESTful

* 當向 Web Server 請求內容時，它是 Get Request
* 當於請求內加入內容，並於回應使用時，它是 Post Request
* 當於請求內更新內容，或者確保一些東西存在的，它是 Put Request
* 當請求刪除時，它是 Delete Request

## Install Flask
~~~
pip install flask
~~~

# 初始化 Flask Web Server
app.py
~~~
from flask import Flask
app = Flask(__name__)
app.run(port=10000, debug=True)
~~~~

# 建立Route
* POST /store data: {name:}
~~~
@app.route('/store' , methods=['POST'])
~~~
* GET /store/<string:name>
~~~
@app.route('/store/<string:name>')
~~~
* GET /store
~~~
@app.route('/store')
~~~
* POST /store<string:name>/item
~~~
@app.route('/store/<string:name>/item' , methods=['POST'])
~~~
* GET /store/<string:name>/item
~~~
@app.route('/store/<string:name>/item')
~~~
