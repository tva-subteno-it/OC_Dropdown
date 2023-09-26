# Dropdown

- [Dropdown](#dropdown)
  - [Introduction](#introduction)
  - [Preview](#preview)
  - [Minimum requirements](#minimum-requirements)
  - [Customization](#customization)
  - [Example](#example)
  - [Other props](#other-props)

## Introduction

This component is a dropdown that allows you to select one or more items from a list. It is fully customizable and can be used in any React project.
In addition to providing a great amount of classes and styles, the component also provides a lot of props to handle the dropdown behavior, such as `onSelectionChange` to handle the selection of an item, or a hidden input to store the selected items.

## Preview

Here you have a preview of the most basic dropdown without any customization.
![img.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img.png?raw=true)

## Minimum requirements

The component requires the following props:
- `items ({id: string; value: string;}[])`: an array of objects containing the items to display in the dropdown. 
- `id (string)`: the id of the hidden input that will store the selected items.
- `label (string)`: the label of the dropdown. Only required if `displayLabel` is true. `displayLabel` is true by default meaning that the label is also required by default.

## Customization

All available class: 

<table>
<tr>
<td>  Code </td> <td> Result </td>
</tr>
<tr>
<td>

```jsx
<DropDown 
    items={items}
     id={"id"}
     label={"Test Label"}
     placeholder={"Test Button"}
     dropdownClass={"border-black"}
     boxClass={"border-red"}
     headerClass={"border-blue"}
     listClass={"border-green"}
     itemClass={"border-purple"}
     labelClass={"color-red"}
/>
```

</td>
<td>

![img_1.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_10.png?raw=true)

</td>
</tr>
</table>

In addition to their corresponding class, you can pass the same attribute with the `style` suffix instead of `class`to customize the dropdown more precisely (e.g `boxStyle` instead of `boxClass`).

<table>
<tr>
<td>  Code </td> <td> Result </td>
</tr>
<tr>
<td>

```jsx                               
 <DropDown                            
  items={items}                        
  id={"id"}                            
  label={"Test Label"}                 
  placeholder={"Test Button"}          
  headerClass={"border-blue"}          
  itemStyle={{backgroundColor: "red"}} 
  />                                   
```    

</td>
<td>

![img.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_9.png?raw=true)

</td>
</tr>
</table>

## Example

<table>
<tr>
<td>  Code </td> <td> Result </td>
</tr>
<tr>
<td>

JSX

```jsx
<DropDown 
    items={items}
     id={"id"}
     label={"Test Label"}
     placeholder={"Test Button"}
     dropdownClass={"dropdown"}
     boxClass={"box"}
     headerClass={"header"}
     headerStyle={{opacity: 1}}
     listClass={"list"}
     itemClass={"item"}
     labelClass={"label"}
     labelStyle={{fontSize: "1.5rem"}}
/>
```

CSS

```css

.dropdown{
    width: 300px;
    margin: 40% auto auto;
}

.box{
    background: darkslateblue;
    border-radius: 4px;
    box-shadow: 0 0 10px rgba(0,0,0,0.5);
}

.header{
    color: white;
}

.list{
    width: 100%;
}

.label{
    color: darkslateblue;
}
.item{
    background: white;
}
```

</td>
<td>

![img_2.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_2.png?raw=true)

</td>
</tr>
</table>


## Other props

- `multiSelect (boolean)`: if true, the dropdown will allow multiple selection. If false, only one item can be selected at a time. The default value is false.

  `multiSelect={true}`: ![img_3.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_3.png?raw=true)

<br/>

- `displayArrow (boolean)`: if true, the arrow icon will be displayed. If false, the arrow icon will be hidden. The default value is true.

  `displayArrow={false}`: ![img_4.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_4.png?raw=true)

<br/>

- `displayLabel (boolean)`: if true, the label will be displayed. If false, the label will be hidden. The default value is true.

  `displayLabel={false}`: ![img_5.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_5.png?raw=true)

<br/>

- `displayReset (boolean)`: if true, the reset button will be displayed. If false, the reset button will be hidden. The default value is true.

  `displayReset={false}`: ![img_6.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_6.png?raw=true)

<br/>


- `position ("top" | "bottom")`: the position of the dropdown box. The default value is bottom.

  `position={"top"}`: ![img_7.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_7.png?raw=true)

<br/>

- `customImage (string)` : change the arrow icon.

  `customImage={"./src/assets/arrow.png"}`: ![img_8.png](https://github.com/tva-subteno-it/OC_Dropdown/blob/main/img/img_8.png?raw=true)
