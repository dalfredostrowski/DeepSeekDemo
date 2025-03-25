http://colab.google.com

#config colab for gpu
# -> connect
# -> change runtime type
# -> set to T4 GPU
# -> "+ code" to get notebook prompt


!pip install colab-xterm


%load_ext colabxterm

%xterm 
curl -fsSL https://ollama.com/install.sh | sh
ollama serve

%xterm
ollama run deepseek-r1:1.5b





# to monitor network for any 'outside' engagement: 
%xterm
watch -n 2 "lsof -i -P -n | grep ollama"
