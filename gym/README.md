# OpenAI Gym
OpenAI Gym是一套可用于开发和比较增强学习算法的工具包， 支持教agents任何事情，比如走路和玩乒乓球、围棋。

##### 应用于强化学习任务的开源接口
开源项目gym为不断成长的强化学习任务提供了一个简单的接口。目前支持Python语言，不久之后会支持其他的开发语言。

    import gym  
    env = gym.make("Taxi-v1")  
    observation = env.reset()  
    for _ in range(1000):  
      env.render()  
      action = env.action_space.sample() # your agent here (this takes  random actions)  
      observation, reward, done, info = env.step(action)  