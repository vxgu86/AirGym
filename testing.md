# 做的改动

setup.py中，install_requires=['keras==2.0.6'],改为==；

D:\RL\AirGym-master\gym_airsim\__init__.py 中打开以下注释。
register(
    id='AirSimEnv-v42',
    entry_point='gym_airsim.envs:AirSimEnv',
)

# todo

test存在问题
dqn.load_weights('dqn_{}_weights.h5f'.format(args.env_name))

ValueError: You are trying to load a weight file containing 2 layers into a model with 0 layers.

用的是keras还是tensorflow.keras? 下次step in试试。

使用要求的2.0.6也没用。


step  reset

        now = airgym.getPosition()
        track = airgym.goal_direction(self.goal, now)
        self.state = airgym.getScreenDepthVis(track)

step   take_action
