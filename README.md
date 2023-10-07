# Anubis
using UnityEngine;

public class DoorController : MonoBehaviour
{
    public float upAmount = 5;
    private void OnTriggerEnter(Collider other)
    {
    }

    private void OnCollisionEnter(Collision other)
    {
        
        if (other.gameObject.CompareTag("Player"))
        {
            Vector3 newPosition = transform.position + Vector3.up * upAmount;
            transform.position = newPosition;
        }
    }
}
 
