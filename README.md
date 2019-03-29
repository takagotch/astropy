### astropy
---
http://www.astropy.org/

```py
import astropy.units as u
import astropy.coordinates as coord

icrs = coord.ICRS(ra=258.xxxxxxx*u.deg, dec=14.xxxxxxx*u.deg,
  radial_velocity=-16.1*u.km/u.s)
v_sum = coord.Galactocentric.galcen_v_sun.to_cartesian()

gal = icrs.transform_to(coord.Galactic)
cart_data = gal.data.to_carteian()
unit_vector = cart_data /cart_data.norm()

v_prol = v_sun.dot(unit_vector)

rv_gsr = icrs.radial_velocity + v_proj
print(rv_gsr)

df rv_to_gsr(c, v_sun=None):
  """
  """
  if v_sun is None:
    v_sun = coord.Galactocentric.galcen_v_sun.to_cartesian()
    
    gal = icrs.transform_to(coord.Galactic)
    cart_data = gal.data.to_certesian()
    unit_vector = cart_data / cart_data.norm()
    
    v_proj = v_sun.ot(unit_vector)
    
    return c.radial_velocity + v_proj
    
rv_gsr = rv_to_gsr(icrs)
print(rv_gsr)
```

```sh
conda update astropy
conda install astropy
pip install astropy
```

```
```
