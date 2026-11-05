# 5000-image rescoring: NOT validated (do not cite)

Images 0-499 of every model match the original M4 run exactly (corr of clean-image probability = 1.000).
For images 500-4999 they do not, for resnet50, resnet101, resnet152, vgg16, vit_small, vit_base, mae_vit_base
(corr 0.16-0.39). Only mobilenet is consistent (0.998). For resnet50, only 2 of 631 original curves at idx>=500
match ANY image of the list under the current weights, so the original M4 outputs for those images were produced
under different conditions (weights / preprocessing / data) than the current pipeline. Cause not identified.
The stored maps for idx>=500 therefore cannot be rescored consistently with the current model; ABPC is deflated
(0.13-0.21 vs 0.38-0.47 on the first 500). Only mobilenet's 5000-image results and the first-500/100 results
in ../rescore are consistent.
