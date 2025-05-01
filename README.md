# Python-for-finance

## Visualization Setup

This snippet configures Matplotlib and Seaborn for high-quality, accessible data visualizations. It optionally boosts figure resolution with `retina` format, suppresses common warnings for cleaner output, and applies a Seaborn theme optimized for presentations (`talk` context) with a colorblind-friendly palette and a default figure size of 12x8 inches. Ideal for financial data analysis or similar projects.

# Optional: Enhance figure resolution for high-quality visuals
%config InlineBackend.figure_format = "retina"

# Import libraries and configure plotting settings
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
from pandas.core.common import SettingWithCopyWarning

# Suppress specific warnings for cleaner output
warnings.simplefilter(action="ignore", category=FutureWarning)
warnings.simplefilter(action="ignore", category=SettingWithCopyWarning)

# Set Seaborn theme for better aesthetics
sns.set_theme(
    context="talk",           # Optimized for presentations
    style="whitegrid",        # Clean grid background
    palette="colorblind",     # Accessible color scheme
    color_codes=True,         # Enable shorthand color codes
    rc={"figure.figsize": [12, 8]}  # Default figure size
)
