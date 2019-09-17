# quartz-demo
1.JobConfigurationHelper类负责从config service 获取配置(同时还监听配置是否change) 并调用JobsFactory类初始化jobs
  通过springboot @ConfigurationProperties注解 类字段映射来获取config service配置，@EventListener(EnvironmentChangeEvent.class)注解来
  监听当config service的配置有改变。
2.一个Job里执行多个task,如PushPriceJob包含获取配置 获取hotelList任务 ，生成event任务 push events任务等

3.目前demo的功能可以实现动态生成job 删除job 修改job配置 ，但集群方面还需要考虑（加全局锁 亦或是 单独一个应用来对jobs进行初始化或管理等）

