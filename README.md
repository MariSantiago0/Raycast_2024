# Raycast_2024
Conceitos de Raycast, Prefabs e Destroy no Unity
<h2> Dupla: Mariana Santiago Matos & Nickolas Garcia Avelino </h2>

    void Update()
    {
        if (Input.GetMouseButtonDown(0))
        
            { 
            // Quando o botão esquerdo é clicado ele vai verificar um hit do raycast
            Ray ray = GetComponent<Camera>().ScreenPointToRay(Input.mousePosition);
            RaycastHit hit;
            if (Physics.Raycast(ray, out hit))
            {
                // Quando for clicado, irá verificar primeiro a tag do gameObject
                string tag = hit.collider.tag;
                GameObject volinho = hit.transform.gameObject;
                // o gameObject foi clicacado e irá fazer uma ação de acordo com a tag especifica
                if (tag == "destroy")
                {
                    Debug.Log("Acertou!");
                    Destroy(bolinho);
                } 
                // Não acertou o gameObject
                else
                {
                    Debug.Log("Errou");
                }
            }
        }
    }
    
<p> O Script está na camera, aonde vai ocorrer a interação com os gameObjects </p>
<h3> Tela do Jogo</h3>
<img src="imgs/telainicial.png">
<p> Os prefabs que foram utilizados foram baixados no asset store </p>
<br>
<p> Assets Baixados: </p> 
 <li> Martelo: https://assetstore.unity.com/packages/3d/props/tools/sledge-hammer-20498 </li>
 <li> Ambiente: https://assetstore.unity.com/packages/3d/environments/fantasy/fantasy-free-260367 </li>
 <li> Gatos: https://assetstore.unity.com/packages/3d/characters/animals/little-friends-cartoon-animals-lite-262505 </li>
 <br>
<p> Link do Projeto no Drive: https://drive.google.com/file/d/1ulRud4pDE5dCI838vr6EVnxl-5obeqHA/view?usp=sharing </p>
<p> Link do Vídeo do Projeto: https://youtu.be/IKbZMjuVUCI </p>
