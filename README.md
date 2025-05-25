# Uzb-force
Kontr
using UnityEngine;

public class CarController : MonoBehaviour
{
    public float speed = 10f;
    public float turnSpeed = 50f;

    void Update()
    {
        float move = Input.GetAxis("Vertical") * speed * Time.deltaTime;
        float turn = Input.GetAxis("Horizontal") * turnSpeed * Time.deltaTime;

        transform.Translate(0, 0, move);
        transform.Rotate(0, turn, 0);
    }
}using UnityEngine;
using UnityEngine.UI;

public class OydinaAI : MonoBehaviour
{
    public InputField userInput;
    public Text chatOutput;

    public void SendMessageToOydina()
    {
        string input = userInput.text.ToLower();

        if (input.Contains("salom"))
            chatOutput.text = "Salom! Sizga qanday yordam beray?";
        else if (input.Contains("missiya"))
            chatOutput.text = "Bugun Namanganda bir qancha topshiriqlar bor. Tayyor bo'ling!";
        else
            chatOutput.text = "Kechirasiz, men buni tushunmadim.";
    }
}using UnityEngine;

public class MissionManager : MonoBehaviour
{
    public bool missionStarted = false;

    public void StartMission()
    {
        missionStarted = true;
        Debug.Log("Missiya boshlandi!");
        // Missiya uchun qo‘shimcha kod yozing
    }

    void Update()
    {
        if (missionStarted)
        {
            // Missiya davomida bajariladigan ishlar
        }
    }
}
