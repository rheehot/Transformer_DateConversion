# torch.nn.Transformer
- encoder input으로 들어가는 data의 padding 처리 방식을 2가지로 구현
	* 구현 1: <https://github.com/hccho2/Transformer_DateConversion/blob/master/DateConversion_Transformer_pytorch/transformer_dateconversion1.py>
		- 입력 data 자체를 공백을 채워 고정길이로 만듬 --> 같은 길이로 만들어졌기 때문에, padding이 필요없다.
	* 구현 2: <https://github.com/hccho2/Transformer_DateConversion/blob/master/DateConversion_Transformer_pytorch/transformer_dateconversion2.py>
		- 입력 data가 길이가 다름. 만들어지는 mini batch내의 sequence는 padding을 통해 길이가 같아지지만, mini batch마다 길이는 달라진다.
		- src_key_padding_mask를 사용하여 encoder input의 paddin된 부분에는 attention이 갈 수 없도록 구현



## torchtext


## Pytorch Transformer API
![torch_transformer](./torch_transformer.png)
- API의 padding이 불필요하게 복잡하다.
- 6개의 padding을 넣어 줄 수 있다.