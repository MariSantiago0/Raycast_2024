# Raycast_2024
Conceitos de Raycast, Prefabs e Destroy

public class raycast : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        Debug.Log("inicio");
    }
    void Update()
    {
        Ray ray = Camera.main.ScreenPointToRay(Input.mousePosition);
        if (Physics.Raycast( ray)){
            Debug.Log("acertou");
        }
        else
        {
            Debug.Log("errou");
        }
    }
}
