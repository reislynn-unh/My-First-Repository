import numpy as np
import matplotlib.pyplot as plt

# Constants
h = 6.626e-34  # Planck's constant (J·s)
c = 3.0e8      # Speed of light (m/s)
k = 1.381e-23  # Boltzmann constant (J/K)

def plancks_law(wavelength, temperature):
    """
    Calculate spectral radiance using Planck's law.
    :param wavelength: Wavelength in meters
    :param temperature: Temperature in Kelvin
    :return: Spectral radiance (W·sr⁻¹·m⁻³)
    """
    numerator = 2 * h * c**2 / wavelength**5
    denominator = np.exp(h * c / (wavelength * k * temperature)) - 1
    return numerator / denominator

# Wavelength range (in meters)
wavelengths = np.linspace(1e-9, 3e-6, 500)  # From 1 nm to 3000 nm

# Temperature (in Kelvin)
temperature = 5800  # Example: Sun's surface temperature

# Calculate spectral radiance
intensities = plancks_law(wavelengths, temperature)

# Plot the results
plt.figure(figsize=(10, 6))
plt.plot(wavelengths * 1e9, intensities, label=f"T = {temperature} K", color="orange")
plt.title("Black Body Radiation Spectrum")
plt.xlabel("Wavelength (nm)")
plt.ylabel("Spectral Radiance (W·sr⁻¹·m⁻³)")
plt.grid(True)
plt.legend()
plt.show()
