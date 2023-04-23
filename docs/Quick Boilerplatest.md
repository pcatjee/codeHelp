---
sidebar_position: 5
---

# Quick BoilerPlates

## React Navigation

**Import:**

```bash
import { useNavigation } from "@react-navigation/native";
```

**Initialization withing main function of the component:**

```bash
const navigation = useNavigation();
```

**Calling it on TouchOpacity:**

```bash
onPress={() => navigation.navigate("Basket")}
```

**Example of back Navigation:**

```bash
onPress={navigation.goBack}
```
