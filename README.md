# Application-of-Python-in-the-Field-of-Water-Supply-Engineering
ASSIGNMENT NO. 08

Q.1) # To determine alkalinity of a given sample
H2SO4_req = float(input("Enter the volume of H2SO4 required in ml: "))
Sample = float(input("Enter the volume of sample in liters: "))
# Calculate alkalinity removed
Alkalinity_Removed = H2SO4_req
print("Alkalinity removed:", Alkalinity_Removed, "mg")

# Calculate total alkalinity in mg/lit
Alk_mg_per_lit = Alkalinity_Removed / Sample
print("Total Alkalinity:", Alk_mg_per_lit, "mg/lit")

# Input OH-Alkalinity present
OH = float(input("Enter the value of OH-Alkalinity present: "))

# Alkalinity removed till pH of 8.3
H2SO4_req_8_3 = float(input("Enter the volume of H2SO4 required to reach pH 8.3 in ml: "))
Alkalinity_Removed_8_3 = H2SO4_req_8_3
print("Alkalinity removed till pH 8.3:", Alkalinity_Removed_8_3, "mg")

# Calculate carbonate alkalinity up to pH 8.3
CO3_Combined = Alkalinity_Removed_8_3 / Sample
print("Carbonate Alkalinity up to pH 8.3:", CO3_Combined, "mg/lit")

# Calculate carbonate alkalinity
CO3 = CO3_Combined - OH
print("Carbonate Alkalinity:", CO3, "mg/lit")

# Calculate bicarbonate alkalinity
HCO3 = Alk_mg_per_lit - 2 * CO3 - OH
print("Bicarbonate Alkalinity:", HCO3, "mg/lit")

OUTPUT:
Enter the volume of H2SO4 required in ml: 30
Enter the volume of sample in liters: 0.2
Alkalinity removed: 30.0 mg
Total Alkalinity: 150.0 mg/lit
Enter the value of OH-Alkalinity present: 5
Enter the volume of H2SO4 required to reach pH 8.3 in ml: 11
Alkalinity removed till pH 8.3: 11.0 mg
Carbonate Alkalinity up to pH 8.3: 55.0 mg/lit
Carbonate Alkalinity: 50.0 mg/lit
Bicarbonate Alkalinity: 45.0 mg/lit
