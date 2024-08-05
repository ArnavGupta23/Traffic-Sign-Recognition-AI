# Traffic Sign Recognition Project

## Experimentation Process

### Initial Model (Test 1)
- **Architecture**: One convolutional layer (32 filters, 3x3 kernel) followed by a max-pooling layer, a fully connected layer with 128 units, and dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.0911, Loss: 7.1538
  - Epoch 10: Accuracy: 0.4428, Loss: 1.7753
  - Final Accuracy: 0.6556, Loss: 0.9989
- **Observation**: The model struggled to converge and had low accuracy, indicating the need for a more complex architecture.

### Test 2
- **Architecture**: Two convolutional layers (32 filters, 3x3 kernel and 64 filters, 3x3 kernel) with max-pooling layers, followed by a fully connected layer with 128 units and dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.1030, Loss: 5.3995
  - Epoch 10: Accuracy: 0.8869, Loss: 0.3694
  - Final Accuracy: 0.9508, Loss: 0.1151
- **Observation**: Adding an additional convolutional layer significantly improved accuracy and convergence.

### Test 3
- **Architecture**: Three convolutional layers (32 filters, 3x3 kernel, 64 filters, 3x3 kernel, 128 filters, 3x3 kernel) with max-pooling layers, followed by a fully connected layer with 128 units and dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.1174, Loss: 5.2580
  - Epoch 10: Accuracy: 0.9291, Loss: 0.2450
  - Final Accuracy: 0.9637, Loss: 0.1383
- **Observation**: Increasing the number of convolutional layers and filters continued to improve model performance.

### Test 4
- **Architecture**: Three convolutional layers (32 filters, 3x3 kernel, 64 filters, 3x3 kernel, 128 filters, 3x3 kernel) with max-pooling layers, followed by two fully connected layers (256 and 128 units) and dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.0867, Loss: 5.3353
  - Epoch 10: Accuracy: 0.9364, Loss: 0.2295
  - Final Accuracy: 0.9670, Loss: 0.1204
- **Observation**: Adding more fully connected layers and dropout further reduced overfitting and improved accuracy.

### Test 5
- **Architecture**: Two convolutional layers (32 filters, 3x3 kernel) with max-pooling layers, followed by two fully connected layers (128 and 64 units) and dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.1513, Loss: 5.7169
  - Epoch 10: Accuracy: 0.9249, Loss: 0.2570
  - Final Accuracy: 0.9583, Loss: 0.1703
- **Observation**: Reducing the number of convolutional layers and adding fully connected layers with dropout still provided good performance but not as high as Test 4.

### Test 6
- **Architecture**: Two convolutional layers (64 filters, 3x3 kernel, 128 filters, 2x2 kernel) with max-pooling layers, followed by dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.3900, Loss: 5.6826
  - Epoch 15: Accuracy: 0.9629, Loss: 0.1768
  - Final Accuracy: 0.9800, Loss: 0.1364
- **Observation**: Increasing the number of epochs to 15 & reduced the dropout to 0.4 improved model performance.

### Test 7
- **Architecture**: Three convolutional layers (64 filters, 3x3 kernel, 128 filters, 2x2 kernel, 256 filters, 3x3 kernel) with max-pooling layers, followed by dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.3800, Loss: 4.0769
  - Epoch 10: Accuracy: 0.9679, Loss: 0.1323
  - Final Accuracy: 0.9809, Loss: 0.0869
- **Observation**: Increasing the model complexity with more filters and layers further improved accuracy.

### Final Model -> Test 8
- **Architecture**: Three convolutional layers (64 filters, 3x3 kernel, 128 filters, 2x2 kernel, 256 filters, 3x3 kernel) with max-pooling layers, followed by a fully connected layer with 512 units and dropout.
- **Performance**:
  - Epoch 1: Accuracy: 0.3598, Loss: 3.5945
  - Epoch 10: Accuracy: 0.9691, Loss: 0.1534
  - Final Accuracy: 0.9838, Loss: 0.0820
- **Observation**: 
  - Adding a fully connected layer with 512 units and dropout resulted in the highest accuracy observed.
  - The final model achieved the highest accuracy with a good balance of complexity, regularization, and no overfitting
- **Architecture**:
  - Three convolutional layers (64 filters, 3x3 kernel, 128 filters, 2x2 kernel, 256 filters, 3x3 kernel) with max-pooling layers.
  - A fully connected layer with 512 units.
  - Dropout to prevent overfitting.
  - Output layer with `NUM_CATEGORIES` units.

## Conclusion
- **What worked well**: Increasing the number of convolutional layers and filters, adding fully connected layers with dropout, and extending the number of epochs significantly improved the model's performance.
- **What didn't work well**: Simplistic architectures with fewer layers and filters struggled to achieve high accuracy. Over complex architectures with too many layers and filters also struggled to achieve high accuracy and low loss.
- **What did I notice**: Regularization techniques such as dropout were crucial in preventing overfitting, especially as the model complexity increased. 

## Additional Documentation
- [Traffic Project Unprocessed Doc](https://docs.google.com/document/d/11bt0XYzP71ZOe8sDgtPoFGbau_hfbUKm0gYuRkWRnYs/edit)