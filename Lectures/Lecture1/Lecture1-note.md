# Lecture 1  Transformers:  An introduction

## what we hope you will learn

    How transformers work
    How they are being applied (beyond just NLP)
    Some new directions of research...

## Attention 的发展历程

以2017 attention is all you need 为分界

之前称为 prehistoric era 主要是RNN以及其变体，seq2seq, lstm 和 GRU, 擅长encoding history信息， 但是对long sequence和context的处理效果很差

2017年之后 on the verge of take-off即将起飞

    realizing the potential in different fields
    solving long sequence problems
        example: protein folding, offline RL
    Few-shot / zero-shot generalization
    Generationg images from language

参考视频 LSTMs are dead, Long live Transformers

未来Future的transformers的情况

    can enable a lot more applications
        Example: Video Understanding , finance
        Generative modeling
    
    Missing ingredients
        External Momory： like neural turing machines
        Reduce computation complexity
        Alignment with language models of human brain

## Attention Mechanisms

Basic Attention (Hard/Soft attention) (Xu et al.
2015)[文章链接](https://glassboxmedicine.com/2019/08/10/learn-to-pay-attention-trainable-visual-attention-in-cnns/)

Learning attention weights

    soft attention: learn attention weight in [0,1] over image patches
                缺点：Expensive computation
    
    
    Hard attention： learn attention weights in {0,1} over image patches
                缺点: 不可微性 (突变数据不可微分）

Basic Attention (local/global attention) (Luong, et al.,
2015)[文章链接](Lectures/Lecture1/Effective_Approaches_to_Attention-based_Neural_Machine_Translation.pdf)

    Global attention models
        similar to soft-attention mechanism
    
    Local attention models
        combinese local hard attention with global soft-attention

Self-Attention (basis of Attention is all you need)

    Scaled dot-product attention
  
    attention = sum(sim(q,k)*v)

    multi-head self-attention

[动图链接](https://towardsdatascience.com/illustrated-self-attention-2d627e33b20a)

other necessary ingredients for the recipe

Positional representations / embedding

Nonlinearities:

Masking

## Encoder-Decoder architecture

Encoder

self-attention layer norm residual connections

good / bad

## applications

GPT-3 Brown et all 2020 BERT