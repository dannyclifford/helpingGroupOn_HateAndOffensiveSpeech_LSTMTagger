# helpingGroupOn_HateAndOffensiveSpeech_LSTMTagger

The notebook explains quite a bit about what I changed and was thinking.

Overall tactics:
1. Remove some ambiguous labeled data where the voter's didn't agree
2. Remove some offensive data from the training samples you're fitting on
3. Use decay in your Adam optimizer
4. Use ModelChecker to save your best model
5. monitor val_loss rather than val_acc so you can make sure you save the best one rather than the last epoch, this will help you have more patience before the loss explodes from overfitting and your model is effected, or models with less accuracy but learned more.
6. train test split twice in order to break up your train, val, and test data
