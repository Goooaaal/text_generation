
## Requirements
- Python 3.6.x
- TensorFlow == 1.5


To train ( utf-8 encoded):
```
python train.py \
  --use_embedding True \
  --input_file data/novel.txt \
  --num_steps 80 \
  --name novel \
  --learning_rate 0.005 \
  --num_seqs 32 \
  --num_layers 3 \
  --embedding_size 256 \
  --lstm_size 256 \
  --max_steps 1000000
```

To sample:
```
python sample.py \
  --converter_path model/novel/converter.pkl \
  --checkpoint_path  model/novel \
  --use_embedding \
  --max_length 2000 \
  --num_layers 3 \
  --lstm_size 256 \
  --embedding_size 256


