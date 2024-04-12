# COMP0124 Coursework: Efficient Social Attention for Autonomous Decision-Making in Varing Traffic Scenarios
This repository contains the source code for coursework paper: Efficient Social Attention for Autonomous Decision-Making in Varing Traffic Scenarios. The experiment environment is forked from: [HighwayEnv](https://github.com/Farama-Foundation/HighwayEnv) and [rl-agents](https://github.com/eleurent/rl-agents).  We modify the code to diploy our proposed method.
## Authors
He Liang, &nbsp;&nbsp;Jianheng Liu, &nbsp;&nbsp;Yunfan Shi
## Modified Code
```
├── rl-agents
│   ├── rl_agents
│   │   ├── agents
│   │   │   ├── common
│   │   │   │   ├── models.py -> introduce sparse attention into the model
│   │   │   ├── deep_q_network
│   │   │   │   ├── pytorch.py -> introduce learnable weight for double q learning
│   ├── scripts
│   │   ├── configs
│   │   │   ├── HighwayEnv
│   │   │   │   ├── env_obs_attention.json          -> Configure the environment observation state
│   │   │   │   ├── agent
│   │   │   │   │   ├── DQNAgent
│   │   │   │   │   │   ├── ego_attention_2h.json   -> Set up the agent's algorithm model
│   │   │   ├── IntersectionEnv
│   │   │   │   ├── env_obs_attention.json
│   │   │   │   ├── agent
│   │   │   │   │   ├── DQNAgent
│   │   │   │   │   │   ├── ego_attention_2h.json
│   │   │   ├── MergeEnv
│   │   │   │   ├── env_obs_attention.json
│   │   │   │   ├── agent
│   │   │   │   │   ├── DQNAgent
│   │   │   │   │   │   ├── ego_attention_2h.json
│   │   │   ├── RoundaboutEnv
│   │   │   │   ├── env_obs_attention.json
│   │   │   │   ├── agent
│   │   │   │   │   ├── DQNAgent
│   │   │   │   │   │   ├── ego_attention_2h.json
```




## License
Code: [MIT License](LICENSE)
