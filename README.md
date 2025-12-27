import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout
from tensorflow.keras.regularizers import l2
from tensorflow.keras.optimizers import Adam

def construir_modelo_riesgo(input_shape):
    """
    Construye una red neuronal para clasificación binaria (Default 0/1).
    Estrategia de Regularización: L2 (Ridge) + Dropout.
    """
    model = Sequential()

    # --- Capa de Entrada + 1ra Capa Oculta ---
    # Calibración: 64 neuronas con activación ReLU para no linealidad.
    # Regularización L2 (Ridge): Penaliza pesos altos para reducir complejidad y Overfitting.
    model.add(Dense(64, activation='relu', input_shape=(input_shape,), 
                    kernel_regularizer=l2(0.01)))
    
    # Dropout (30%): Desactiva neuronas aleatoriamente durante el entrenamiento
    # para forzar a la red a aprender características robustas.
    model.add(Dropout(0.3))

    # --- 2da Capa Oculta (Deep Learning) ---
    model.add(Dense(32, activation='relu', kernel_regularizer=l2(0.01)))
    model.add(Dropout(0.3))

    # --- Capa de Salida ---
    # Sigmoide: Para obtener una probabilidad entre 0 y 1.
    model.add(Dense(1, activation='sigmoid'))

    return model
