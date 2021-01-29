using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SimpleMoveMouse : MonoBehaviour
{

	private float speed = 2.0f;

	Animator anim;

	private Vector3 lastPosition;

	// Start is called before the first frame update
	void Start()
    {
		anim = GetComponent<Animator>();
		lastPosition = transform.position;
    }

    // Update is called once per frame
    void Update()
    {
		if (Input.GetKey(KeyCode.RightArrow))
		{
			transform.position += Vector3.right * speed * Time.deltaTime;
		}
		if (Input.GetKey(KeyCode.LeftArrow))
		{
			transform.position += Vector3.left * speed * Time.deltaTime;
		}
		if (Input.GetKey(KeyCode.UpArrow))
		{
			transform.position += Vector3.forward * speed * Time.deltaTime;
		}
		if (Input.GetKey(KeyCode.DownArrow))
		{
			transform.position += Vector3.back * speed * Time.deltaTime;
		}


		float wd = Vector3.Distance(transform.position, lastPosition) / Time.deltaTime;
		print(wd);

		anim.SetFloat("WalkedDistance", wd);

		lastPosition = transform.position;


	}
