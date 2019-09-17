# quartz-demo
1.JobConfigurationHelper类负责从config service 获取配置(同时还监听配置是否change) 并调用JobsFactory类初始化jobs

2.一个Job里执行多个task,如PushPriceJob包含获取配置 获取hotelList任务 ，生成event任务 push events任务等

