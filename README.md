# ProjetoFinal-Computacao-em-GPU

# 📌 Filtros de Imagem com GPU

&#x20;

> Implementação de diversos filtros de imagem utilizando GPU com CuPy e Numba para o processamento de imagens biométricas.

## 🚀 Tecnologias Utilizadas

- 🖥️ OpenCV
- ⚡ CuPy
- 🔥 Numba CUDA
- 🏞️ skimage (SSIM)
- 📊 NumPy

## 📦 Como Usar no Google Colab

1. Acesse o Google Colab e crie um novo notebook.
2. Instale as dependências necessárias no ambiente executando:
   ```python
   !uv pip install -q --system numba-cuda==0.4.0
   ```
  3. Faça o upload do arquivo de código no Colab.
4. Execute as células do notebook para aplicar os filtros e visualizar os resultados.

## ✅ Funcionalidades

- ✅ Aplicação de filtros na GPU usando CuPy e Numba
- ✅ Filtro Gaussiano (borramento)
- ✅ Filtro Laplaciano (detecção de bordas)
- ✅ Filtro de nitidez (com combinação de suavização)
- ✅ Filtro Sobel combinado (detecção de bordas)
- ✅ Cálculo de métricas: SNR e SSIM

## 📸 Demonstração

![demo](https://github.com/user-attachments/assets/83809761-8e64-4db4-97e5-c8de889784ab)

## 📊 Resultados
![image](https://github.com/user-attachments/assets/5d585234-deaf-42ac-90ee-bf6c75d059f6)

### 🟢 Filtro Gaussiano (Borramento)
- **SNR:** 27.083 → O filtro Gaussiano preservou grande parte do sinal original enquanto reduziu o ruído.  
- **SSIM:** 0.955 → A imagem borrada mantém alta semelhança estrutural com a original.  

**🔎 Conclusão:** O filtro Gaussiano demonstrou ser o mais eficaz para preservar a estrutura da imagem enquanto suaviza o ruído.  

---

### 🔵 Filtro Sobel (Detecção de Bordas)
- **SNR:** 20.166 → A combinação da imagem original com as bordas detectadas pelo Sobel preservou as informações do sinal original.  
- **SSIM:** 0.823 → A imagem resultante é estruturalmente muito semelhante à original.  

**🔎 Conclusão:** A detecção de bordas com o filtro Sobel foi eficaz, resultando em uma imagem que preserva mais informações e mantém boa similaridade estrutural com a original.  

---

### 🟠 Filtro de Nitidez
- **SNR:** 15.965 → O SNR reduzido era esperado, pois o filtro de nitidez introduz um leve ruído ao realçar os detalhes.  
- **SSIM:** 0.908 → A imagem com nitidez aumentada é um pouco mais semelhante à original em termos estruturais.  

**🔎 Conclusão:** O filtro de nitidez manteve um bom desempenho, com uma leve melhoria na similaridade estrutural, apesar do aumento do ruído.  

---

📌 *Essas métricas indicam como cada filtro impacta a imagem em termos de preservação da estrutura e redução de ruído. Dependendo do objetivo da aplicação, um filtro pode ser mais adequado que outro.* 



## Exemplo de aplicação dentro do Projeto

🔹 Em posse do segmentador "SEGV4.h5" disponibilizado pela empresa NatoSafe, foi possível obter um resultado mais satisfatório com a utilização por exemplo do Filtro Sobel (detecção de bordas).
Percebe-se que o segmentador conseguiu atuar melhor e cumprir seu papel em mais regiões da imagem.


![frame_1_seg](https://github.com/user-attachments/assets/ad712721-d5cf-424e-950b-0caa759cfe5d)


![edges_sobel_seg](https://github.com/user-attachments/assets/61163de3-3be1-480c-a2b6-439649c6b4bb)




## 📜 Licença



Feito com ❤️ por [Wesley](https://github.com/WesleyCatuzzo)!




 
