# b1k-baselines
Repo for running various baselines with Behavior-1K

# evaluation

- serve the policy
```bash
cd ~/b1k-baselines/baselines/openpi
source .venv/bin/activate
uv run scripts/serve_b1k.py --task_name=picking_up_trash policy:checkpoint --policy.config=pi05_b1k --policy.dir=/home/xhz/outputs/checkpoints/pi05_b1k/picking_up_trash/49999
```

- run the evaluation
```bash
cd ~/BEHAVIOR-1K/
conda activate behavior 
python OmniGibson/omnigibson/learning/eval.py policy=websocket task.name=picking_up_trash log_path=/home/xhz/logs/pi05/picking_up_trash/49999
```