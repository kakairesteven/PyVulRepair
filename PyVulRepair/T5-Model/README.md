To reproduce the results of our PyVulRepair **(Inference only)**:
```
python PyVulRepair.py \
    --output_dir=./saved_models \
    --model_name=model.bin \
    --tokenizer_name=AfricaKing/PyVulRepair \
    --model_name_or_path=AfricaKing/PyVulRepair \
    --do_test \
    --encoder_block_size 512 \
    --decoder_block_size 256 \
    --num_beams=50 \
    --eval_batch_size 1
```
Note. please adjust the "num_beams" parameters (i.e., num_beams= 1, 2, 3, 4, 5, 10)

To retrain this model from scratch, run the following commands **(Training only)**:
```
python PyVulRepair.py \
    --model_name=model.bin \
    --output_dir=./saved_models \
    --tokenizer_name=Salesforce/codet5-base \
    --model_name_or_path=Salesforce/codet5-base \
    --do_train \
    --epochs 75 \
    --encoder_block_size 512 \
    --decoder_block_size 256 \
    --train_batch_size 8 \
    --eval_batch_size 8 \
    --learning_rate 2e-5 \
    --max_grad_norm 1.0 \
    --evaluate_during_training \
    --seed 123456  2>&1 | tee train.log
```
