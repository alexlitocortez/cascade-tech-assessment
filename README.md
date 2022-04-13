# cascade-tech-assessment

Financial Statement Component

This project is an assessment for Cascade Fintech. The goal was to make a component displaying the financial information.

#SOLUTION

1. The first step was to figure out how to integrate the data into the project. Since it was already in JSON format, I created a local JSON file so we can retrieve it in our component.

2. The second step was to figure out how to make sure the data we are retrieving in our component is working. I did this by implementing a function doing console.log.

3. After the data is retrieved, I used a "v-for" to loop over the data.

4. Once the third step is done, I had to display the data. Accessing a multi-layered object was different for me but I just used dot notation. The tricky part is to remember the key values are case sensitive so I had to capitalize when necessary to access specific information.

5. After the 4th step, everything else was creating divs that used flexbox. This made sure the content was horizontal when the screen is bigger than 1250 pixels and vertical once the screen was smaller than 1250 pixels.
