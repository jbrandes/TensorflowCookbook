# TensorflowCookbook
Run this script to create real recipes created by tensorflow machine learning on python. 

Before running the full script make sure to train your data. Put in this code first and run desired number of epoches to get loss rate down. Once that is done take out the compile part and run the rest of the code with the lowest training checkpoint, usually the last one.

model.compile(optimizer='adam', loss=loss)

Configure checkpoints

Use a tf.keras.callbacks.ModelCheckpoint to ensure that checkpoints are saved during training:

# Directory where the checkpoints will be saved
checkpoint_dir = './training_checkpoints'
# Name of the checkpoint files
checkpoint_prefix = os.path.join(checkpoint_dir, "ckpt_{epoch}")

checkpoint_callback=tf.keras.callbacks.ModelCheckpoint(
    filepath=checkpoint_prefix,
    save_weights_only=True)

