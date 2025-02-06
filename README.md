# 🤖 ML-Agent-Fundamentals
A beginner-friendly guide to Unity ML-Agents reinforcement learning

## 🎯 Overview
This project demonstrates how to create and train an intelligent agent using Unity ML-Agents. Watch as your agent learns to navigate and find goals through reinforcement learning! Perfect for developers getting started with ML-Agents.

## ✨ Features
- 🎮 Simple environment setup for ML-Agents
- 🧠 Basic reinforcement learning implementation
- 🎯 Goal-seeking behavior training
- 📊 Training configuration examples
- 🔄 Easy-to-understand training loop

## 🛠️ Prerequisites
- Unity 2020.3 or later
- Python 3.6 or later
- ML-Agents Release 2.0 or later

## 📦 Installation

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/ML-Agent-Fundamentals.git
cd ML-Agent-Fundamentals
```

2. **Install Python Dependencies**
```bash
pip install mlagents
pip install torch
```

3. **Unity Setup**
- Open Unity Hub
- Add project from disk
- Install required Unity version if prompted
- Open project

## 🚀 Getting Started

1. **Open the Demo Scene**
- Navigate to `Assets/Scenes`
- Open `TrainingScene`

2. **Configure the Environment**
```yaml
behaviors:
  GoalSeeker:
    trainer_type: ppo
    hyperparameters:
      batch_size: 64
      buffer_size: 12000
      learning_rate: 0.0003
    network_settings:
      normalize: true
      hidden_units: 128
      num_layers: 2
    reward_signals:
      extrinsic:
        strength: 1.0
```

3. **Start Training**
```bash
mlagents-learn config/trainer_config.yaml --run-id=first_training
```

## 🎮 Project Structure
```
ML-Agent-Fundamentals/
├── Assets/
│   ├── Scripts/
│   │   ├── GoalSeekerAgent.cs
│   │   └── EnvironmentController.cs
│   ├── Scenes/
│   │   └── TrainingScene
│   └── Prefabs/
├── config/
│   └── trainer_config.yaml
└── README.md
```

## 📝 Key Components

### GoalSeekerAgent Script
The main agent script that handles:
- 👁️ Observations
- 🎯 Actions
- 🏆 Rewards
- 🔄 Environment reset

```csharp
public class GoalSeekerAgent : Agent
{
    public override void CollectObservations(VectorSensor sensor)
    {
        // Add observations here
    }

    public override void OnActionReceived(ActionBuffers actions)
    {
        // Handle actions and rewards here
    }
}
```

## 📊 Training Process

1. **Environment Setup**
   - Create training area
   - Place agent and goals
   - Configure observations and rewards

2. **Training Configuration**
   - Adjust hyperparameters
   - Set network architecture
   - Define reward signals

3. **Training Loop**
   - Run training sessions
   - Monitor progress
   - Adjust parameters as needed

## 🔗 Useful Links
- [ML-Agents Documentation](https://github.com/Unity-Technologies/ml-agents)
- [Unity Learn](https://learn.unity.com/)
- [ML-Agents Forum](https://forum.unity.com/forums/ml-agents.453/)
