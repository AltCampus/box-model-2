# Advanced Box Model

## Topics of the day

1. Box Sizing
   - Content Box
   - Border Box
   - Deciding between the box-sizing.
2. Outline
3. Box Shadow

## 1. Box Sizing

Till now we have seen all the properties of the box model and how all these properties work and defined. By default, we have also seen that the box model properties are additive. Remember in the previous section, how the size of the box increased as we add the padding, borders, margins. This is the default behaviour of the box model. If you specify any width to the element and then after if you add any padding, or borders or margins, then you will have to add these properties in your specified width.
We can change this default additive behaviour of the box model. In CSS3 we have new box-sizing property, which allows us to change the box model. It gives us the options, how we want to calculate the size of the box.
Box Sizing property comes with two values: `content-box and border-box`. Both the boxes are slightly different from each other. Let's see them one by one.

### Content Box

Content box is the default value for the `box-sizing` property. It leaves the model additive only.

```
  div {
    box-sizing: content-box;
  }
```

In content box after the width and height, whatever the extra properties`padding, borders, or margins` we define will get added to the specified size of the box. If we don't specify any box-sizing property this will be the default value for all the elements.

### Border Box

Border box value changes the box model. It keeps the padding and border within the specified width and height. If an element has a width of 300px, padding of 20px, and border around it is 10px, if we make the box as a border-box then the actual width will remain 300px.

```
  div {
    width: 300px;
    padding: 20px;
    border: 10px solid #272727;
    box-sizing: border-box;
  }
```

So, here according to the border-box value the div will be having a width of 300px instead of 360px.

But if we add any margin it will be added to the specified width of the element. So, in both the cases whether it is a content-box or a border-box, the margins are always added to calculate the actual size of the box.

### Choosing between content-box and border-box.

Now, I know there will be confusion while choosing a box-sizing value. Generally, you should choose a border-box, because it keeps things simpler and easier. You will not have to do the math for calculating the actual size of the box, whatever the size you will specify it will always remain that much only.

## 13. Outline

The outline is similar to a border but stays outside the border. The way define border for an element in a similar way we can draw an outline. But the important point is that the outline is not considered as part of the box model. So it does not increases the dimensions of the box.

```
  div {
    outline: 4px solid red;
  }
```

## 14. Box Shadow

There is one more property here i.e. box-shadow, but similar to outline, this is also not considered as a part of the box model. It is used just to create a shadow effect around the element.

```
  div {
    box-shadow: 3px 3px 6px 1px rgba(0, 0, 0, 0.3);
  }
```

The property generally accepts five values. The first four values are for creating length and height of shadow and the last value is for the color of the shadow.
In the values, the first value is for the shadow's offset in the horizontal direction, the second value is for the shadow's offset in the vertical direction, the third value is for blur radius. The third value determines how blurry the shadow will look. The fourth value is to spread the shadow in all direction. This is the optional value, without this also we can create a shadow.

```
  div {
    box-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
  }
```

We can also create multiple shadows on one element. To create multiple shadows just need to add comma separated values.

```
  div {
    box-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3), 6px 6px 10px rgba(0, 0, 0, 0.3);
  }
```

If we provide the values in negative then it will create a shadow in the opposite direction.

```
  div {
    box-shadow: -3px -3px 6px rgba(0, 0, 0, 0.3);
  }
```

We can also create some solid line around the box using box-shadow.

```
  div {
    box-shadow: 0 0 0 3px #000;
  }
```

The above value will create solid line around the element instead of any shadow effect.

All the above box-shadow values will create the shadow outside the box, but if you want to create the shadow inside the box you can just add inset at the starting of the value.

```
div {
  box-shadow: inset 3px 3px 6px rgba(0, 0, 0, 0.3);
}
```

## Answer the following questions

1. How can we avoid the expansion of the element if we add any border or padding?
2. What are the box-sizing properties?
3. How can we add box-shadow?
4. Create a solid line inside the box using box-shadow.

## Do the exercises

## DO the project 1

## Do the pair programming

## Additional Resources

1. https://learn.shayhowe.com/html-css/opening-the-box-model/

- https://internetingishard.com/html-and-css/css-box-model/
