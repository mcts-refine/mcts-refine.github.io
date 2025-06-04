---
icon: fas fa-tag
order: 1
---

## Downloads
[**MCTS-Refine**](https://github.com/mcts-refine/mcts-refine-code)
## Run Piecer
- Step 1

Download the source code and install the requirements.
```python
pip install requirements.txt
```
- Step 2

Sepcific the argument in ```run_mcts.py```

```python
    parser = argparse.ArgumentParser(description="MCTS任务执行脚本")
    parser.add_argument("--model", type=str, default=r"deepseek", help="Model Generated CoT")
    parser.add_argument("--reward_model", type=str, default=r"deepseek", help="Reward Model")
    parser.add_argument("--task_ids", type=str, help="Path to Task IDs",
                        default=r"...\batch_1.txt")
    parser.add_argument("--repo_base", type=str, default=r"...\clone_repos",
                        help="Repo Path")
    parser.add_argument("--json_path", type=str, default=r"SWE-Fixer-Train-110K",
                        help="SWE-Fixer")
    parser.add_argument("--log_dir", type=str, default=r"...\save_cot",
                        help="Save Path")
    parser.add_argument("--task_type",
                        choices=['locate_file', 'locate_code_snippet',
                                 'code_generation'],
                        default='locate_file')
```
