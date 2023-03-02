Programa de propostas de orçamento 

(Adicionar ao código)

 string nome_ficheiro = "Precos_Material.cvs"
    if(nome_ficheiro.empty()==true){
        cout << "Ficheiro não encontrado. Verificar se Precos_Material.cvs existe"
    }
    
    string str;
    ifstream f(nome_ficheiro);

  while(getline(f,str)){
        stringstream s;
        s<<str;
        string aux;
        vector <string> ax;
        while(s.good()){
            getline(s,aux,',');
            ax.push_back(aux);
        }
 
  cout << "Nome do material em causa? (Tem de estar de acordo com o criado no ficheiro!!)" <<endl;
  cin >> material;
 
  for (int j=0; j<ax.size()/2; j=j+2){
    int d=0;
    if(strcmp(ax[j], material)==0){
       d=1;
       cout << "Preço do materail é: << ax[j+1] <<"?" (S/N)}
       cin >> confirmação;
       if (confirmação=='N'){
       cout << "Qual o preço?" << endl;
        cin >> preco;
        d==-1;
    }
    }
    
if(d==0){
    cout << "Material não existe! Quer adicionar?" << endl;
    cout << "Nome do material?"
    cin >> material;
    cout << "Preço do material?"
    cin >> preco;
    (escrever código de escrita no ficheiro)
    }
if(d==-1){
    (escrever código de escrita no ficheiro)
    }
    
