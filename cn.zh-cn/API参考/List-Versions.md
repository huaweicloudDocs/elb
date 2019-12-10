# List Versions<a name="zh-cn_topic_0109430491"></a>

## 功能介绍<a name="zh-cn_topic_0049143278_section64833508"></a>

查询当前所有可用的版本。

如果访问Neutron服务的url中不添加版本信息，neutron返回当前所有可用的版本。

## URI<a name="zh-cn_topic_0049143278_section46630661"></a>

GET /

## 请求消息<a name="zh-cn_topic_0049143278_section17022773"></a>

无

## 响应消息<a name="zh-cn_topic_0049143278_section18987236"></a>

无

## 示例<a name="section1481434242515"></a>

-   请求样例

    ```
    GET /
    ```


-   响应样例

    ```
    {
       "versions": [
          {
              "status": "CURRENT",
              "id": "v2.0",
              "links": [
             {
                "href": "http://192.168.82.231:9696/v2.0",
                "rel": "self"
             }
            ]
           }
         ]
    }
    ```


