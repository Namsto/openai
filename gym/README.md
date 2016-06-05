# OpenAI Gym
原文链接：[https://gym.openai.com/](https://gym.openai.com/)
OpenAI Gym是一套可用于开发和比较强化学习算法的工具包， 支持教agents任何事情，比如走路和玩乒乓球、围棋等。

### 应用于强化学习任务的开源接口
开源项目gym为不断成长的强化学习任务提供了一个简单的接口。目前支持Python语言，不久之后会支持其他的开发语言。
```python
    import gym  
    env = gym.make("Taxi-v1")  
    observation = env.reset()  
    for _ in range(1000):  
      env.render()  
      action = env.action_space.sample() *# your agent here (this takes  random actions)*  
      observation, reward, done, info = env.step(action)  
```  
      
### 我们提供环境，你提供算法
开发者可以使用TensorFlow或Theano等已存在的算法库来实现agent。

### 分享和比较结果
OpenAI Gym支持开发者上传测试结果、意见或建议，同时支持重现他人的结果。每个任务都会被标记上版本号来确保结果具有可比较性。
```python
    import gym  
    env = gym.make("FrozenLake-v0")  
    env.monitor.start("/tmp/gym-results")  
    observation = env.reset()  
    for _ in range(1000):  
      env.render()  
      action = env.action_space.sample() *# your agent here (this takes random actions)*  
      observation, reward, done, info = env.step(action)  
    env.monitor.close()  
    gym.upload("/tmp/gym-results", algorithm_id="random", api_key="sk_AKoNu8JTQdKnRmWOqGFPug")  
```
### 新的工作方法
任何人都与我们合作，做出最佳的效果，那样你会知道每项任务的最新状态。