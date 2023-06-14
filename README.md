# ImageImprov

## Usage
Tip:
-  The h/w resolution of all input images shall be divided by 4, such as 600*400.

### Testing

To test the pre-trained model on LOL dataset, just run:
```
bash test.sh
```

or run:

```
python test.py  --test_folder  path_to_images  --output save_images_here  --modelfile pretrained_model --modeltype lol
```
Example:
```
python test.py  --test_folder  ./datasets/LOL/test/low  --output  ./output_test  --modelfile ./model_LOL.pth --modeltype LOL
```
- You can change the `--test_folder` to test your own dataset.
- You can use the pretrained model training on Adobe-MIT FiveK dataset by `--modelfile ./model_FIVEK.pth --modeltype FIVEK`

To train the model, just run:

```
bash train.sh
```
or run:
```
python train.py --trainset  path_to_trainset  --testset path_to_testset  --output  save_inter_images
```
Example:
```
python train.py --trainset  ./datasets/LOL/train  --testset  ./datasets/LOL/test  --output  ./output
```
