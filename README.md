# Dropdown

## Usage

Dropdown component is used to display a list of items in a dropdown box. It can be used to select a single item or multiple items.

You can choose where to display the dropdown box by passing the `position` prop. The default position is bottom.

You can choose to display the arrow icon by passing the `displayArrow` prop. The default value is true.

You have many customization options for the whole dropdown, header and list. You can pass the `dropdownClass`, `boxClass`,  `headerClass` and `listClass` props to customize the whole dropdown (input + list + label, input + list, input, and list respectively).

In addition to the classes, you can pass their corresponding styles (e.g `boxStyle`) prop to customize more precisely the dropdown.

Some classes are already defined but unused to give you the possibility to customize the dropdown as you want :
- `dropdown_backdrop`
- `dropdown_container`
- `dropdown`
- `dropdown__header`
- `dropdown__header__title`
- `dropdown__header__icon`
- `dropdown__list`
- `dropdown__list__item`
- `dropdown__list__item`

This dropdown contains a hidden input that will be used to store the selected items. You can pass the `id` prop to customize the id of this input. Every selected items is joined by a comma.

A `onSelectionChange` prop ca be passed to the dropdown. It will be called every time the selection changes. It will return the selected items.

```jsx
<DropDown id={id} label={label} items={data} multiSelect={false} displayArrow={true}
          dropdownClass={"mt-4 w-full"}
          boxClass={"bg-primary bg-opacity-10"}
          boxStyle={{border: "1px solid rgba(40, 25, 14, 0.20)"}}
          headerClass={"text-black"}
          listClass={"bg-[#eef0e5] w-full"}
          placeholder={placeholder}
          position={position}
/>
```