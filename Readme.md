<H1>CHARACTER LEVEL RNN TRAINED ON TINY SHAKESPEARE DATASET</H1>

<p>The weights of the model are available in the rnn_weight_torch_2.pth</p>
<p>This is just a experimental model created to appease my curiosity and learn the RNN properly</p>

<h2>FEATURES : </h2>
<li>1 Hidden layer with 100 neurons</li><br>
<li>
    For training this model, the context window of size 10 is used. This means it will look at the 10 previous charactersß before prediciting the 11th character
<li><br>
<li>
    The weigths of the model are initialized using manual implemenetation of Xavier init method, which are proven to provide great various for weights if tanh non-linear activation are used.
</li><br>
<li>
    Initially batch size of 32 was used for training.
    The 256 and finally 512
    A hyperparameter tuning like table is given below
</li><br>
<li>
    Initially the training was done for 50 epochs with batch size of 32 and 256.
    with 1 million entries in X_train, it means:
    <br>
    For 30 epochs :
    model sees 3906 examples per epoch for 256 batch size
    and 1961 for 512 batch size.
</li><br>
<li>
    The Final validation loss is 1.736. Maybe the loss would decrease if I further enhance the model by: increasing the embedding size, increasing the context window and modifying the hidden network. But I think this should suffice for a char level RNN. I will try that with the word level model.
</li><br>

<h2> Parameter Tables</h2>
![image] (readme_img.png)

<br>
<p> The weights of the final model are present in 'rnn_wieght_torch-3.pth' file</p>