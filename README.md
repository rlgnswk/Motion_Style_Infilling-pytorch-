# Motion_Style_Infilling-pytorch-
Motion_Style_Infilling(pytorch) / GCT525 Motion Graphics Term project







기록.





Batch norm을 넣어서 학습이 안정되었다. 이전에 특정 시점에서 갑자기 값이 튀는 문제 발생.



AE는 infilling이 어느정도 잘 됨.
Decoder에 BN 빼도 어느정도 잘됨 -> 좀 가만히 있지를 못하는거 같기도? 흔들림. 떨리는거랑 조금 다르게


VAE로 하니까 결과가 떨림.


StyleTransfer
AdaIN은 일단 Non pretrained시 아주 이상한 결과가 나옴
하지만 확인한하고 갖다 붙여서 한거니까 다시 들여다볼 필요는 있음.

recon 1.0 일떄 (style loss x ) A-> A는 잘 되는편

하지만 Style 반 contetn 반이 명확하게 가이드 되지않음

recon weight넣어서 줄이니까 움직이지도 않음.

디노이징(빈칸 x , 노이즈만 첨가)은 VAE, AE 모두 잘 됨

GANbased는 일단 학습이 안됨 그냥 서있음.

selfRef_sameWeights 뭔가 망가지진 않는데, 뭘 보고 배우는지 모르겠음 하나의 인풋 하나의 스타일로 매칭되는 결과는 아님.

baseline으로 motion blending한거를 사용해야 할수도 있음 . -> VAE로 가정 넣어서 latent space에서 affine transform ㄱㄱ