ITU GenAI RAG Workshop

Bu depo, Retrieval-Augmented Generation (RAG) tekniğini kullanarak OpenAI'ye istek gönderen bir Jupyter Notebook dosyasını içermektedir. Dosya, OpenAI'nin dil modellerini kullanarak dış bir bilgi kaynağı (knowledge base) ile genişletilmiş yanıtlar üretmek için tasarlanmıştır.

📌 İçerik

  OpenAI API kullanımı

  RAG (Retrieval-Augmented Generation) yöntemiyle bilgi tabanından veri çekme

  PDF formatındaki bir knowledge base'in işlenmesi

  Google Colab üzerinde çalıştırma yönergeleri

🚀 Başlangıç

  Bu projeyi çalıştırmak için Google Colab'i kullanmanız gerekmektedir.

  1️⃣ Google Colab'e Dosyayı Aktarın

    ITU_GenAI_RAG_Workshop.ipynb dosyasını Google Colab'e yükleyin.

    Google Drive'ınızı Colab'e bağlayarak dosyaları daha kolay yönetebilirsiniz.

  2️⃣ Knowledge Base Dosyasını Yükleyin

    data/ klasöründe bulunan knowledge base PDF dosyasını Google Colab çalışma dizinine yükleyin.

    Bunun için Colab'de aşağıdaki komutu çalıştırabilirsiniz:
    
    from google.colab import files
    uploaded = files.upload()
    
    Alternatif olarak, dosyayı Google Drive'ınıza yükleyerek Colab içinde bağlayabilirsiniz:
    
    from google.colab import drive
    drive.mount('/content/drive')
  
  3️⃣ OpenAI API Anahtarını Tanımlayın
  
    Bu proje, OpenAI API kullanarak RAG modeliyle metin oluşturma işlemi yapmaktadır. API anahtarınızı tanımlamak için:
    
    OpenAI hesabınıza giriş yaparak API anahtarınızı alın: https://platform.openai.com/signup/
    
    Notebook içinde aşağıdaki kodu çalıştırarak API anahtarınızı tanımlayın:
    
    import openai
    openai.api_key = "SİZİN_OPENAI_API_ANAHTARINIZ"
    
    veya güvenli bir yöntem olarak Colab'in gizli değişkenlerini kullanabilirsiniz:
    
    import os
    os.environ["OPENAI_API_KEY"] = "SİZİN_OPENAI_API_ANAHTARINIZ"

  4️⃣ Notebook'u Çalıştırın
  
    Tüm adımları tamamladıktan sonra, ITU_GenAI_RAG_Workshop.ipynb dosyasını adım adım çalıştırabilirsiniz.


🛠️ Kullanılan Teknolojiler

  OpenAI GPT API – Metin üretimi için
  
  Google Colab – Çalışma ortamı olarak
  
  LangChain – RAG uygulaması için
  
  PyPDF – PDF dosyalarını işlemek için
