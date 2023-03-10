## 使用说明(coordTransform_utils.py)

```bash
gcj02_to_bd09(lng, lat) # 火星坐标系->百度坐标系
bd09_to_gcj02(lng, lat) # 百度坐标系->火星坐标系
wgs84_to_gcj02(lng, lat) # WGS84坐标系->火星坐标系
gcj02_to_wgs84(lng, lat) # 火星坐标系->WGS84坐标系
bd09_to_wgs84(lng, lat) # 百度坐标系->WGS84坐标系
wgs84_to_bd09(lng, lat) # WGS84坐标系->百度坐标系
```

## 批量转换csv文件使用说明(coord_converter.py)
### 示例

```bash
# 不指定经纬度列名（默认为'lng', 'lat'）
$ python coord_converter.py -i test_input.csv -o test_output.csv -t b2g

# 指定经纬度列名
$ python coord_converter.py -i test_input.csv -o test_output.csv -t b2g -n 经度 -a 纬度

# 跳过无效经纬度的行（默认不跳过）
$ python coord_converter.py -i test_input.csv -o test_output.csv -t b2g -n 经度 -a 纬度 -s True
```


```bash
# 查看使用帮助
$ python coord_converter.py -h

usage: coord_converter.py [-h] -i INPUT -o OUTPUT -t TYPE [-n LNG_COLUMN] [-a LAT_COLUMN] [-s SKIP_INVALID_ROW]

Convert coordinates in csv files.

optional arguments:
  -h, --help            show this help message and exit

arguments:
  -i , --input          Location of input file
  -o , --output         Location of output file
  -t , --type           Convert type, must be one of: g2b, b2g, w2g, g2w, b2w,
                        w2b
  -n , --lng_column     Column name for longitude (default: lng)
  -a , --lat_column     Column name for latitude (default: lat)
  -s , --skip_invalid_row
                        Whether to skip invalid row (default: False)
```


