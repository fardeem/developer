# smol developer

a fork of swyx's [smol developer](https://github.com/smol-ai/developer). Trying out new ways of extending it.


## running

```bash
pip install modal-client
modal token new

modal run main.py --prompt flask.md

modal run debugger.py --prompt flask.md
```

## notes

if you don't set a `concurrency_limit` on calling the api you get rate limited by openai. It works with

- `n = 10` for the flask prompt and takes 2 mins, 
- `n = 5` and takes ~4 mins
- `n = 20` also took ~2 mins so I think at that point open ai's API becomes the rate limiting factor