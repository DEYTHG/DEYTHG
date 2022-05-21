import matplotlib.pyplot as plt
from matplotlib.cm import ScalarMappable
from mpl_toolkits.basemap import Basemap
from matplotlib.animation import FuncAnimation


### Create a figure and draw a basemap
fig, ax = plt.subplots(figsize=(10,8), dpi=500)

m = Basemap(resolution='h',
            projection='lcc',
            lat_0=11.9, lon_0=122.5,
            llcrnrlon=117, llcrnrlat= 5, urcrnrlon=127, urcrnrlat=19)
m.drawcoastlines()
m.drawmapboundary(zorder=0)
m.fillcontinents(color='#ffffff',zorder=1)
m.drawcountries(linewidth=1.5)
m.drawstates()
