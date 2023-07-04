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


