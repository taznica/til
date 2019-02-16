# Change the color of GameObject in script

Version: 2017.4

---

To change the color of GameObject:

```.cs
GetComponent<Renderer>().material.color = Color.red;
```

If you wanto to use RGBA instead:

```.cs
GetComponent<Renderer>().material.color = new Color32(255, 0, 0, 1);
```

Or:

```.cs
GetComponent<Renderer>().material.color = new Color(1.0f, 0.0f, 0.0f, 1.0f);
```

---

### References:

[Unity DOCUMENTATION - GameObject.renderer](https://docs.unity3d.com/2017.4/Documentation/ScriptReference/GameObject-renderer.html)

[Unity DOCUMENTATION - Color32](https://docs.unity3d.com/2017.4/Documentation/ScriptReference/Color32.html)

[Unity DOCUMENTATION - Color](https://docs.unity3d.com/2017.4/Documentation/ScriptReference/Color.html)
