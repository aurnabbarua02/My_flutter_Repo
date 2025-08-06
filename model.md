# Model format

```dart

Class Model{
  String? data;
  CustomData customData;
  List<CustomData> customList;
  Model({this.data, this.customData, this.custom});
  factory Model.fromJson(Map<String, dynamic> json) =>
        Model(
              data: json['data'] ?? "",
              customData: CustomData.fromJson(json['customData']),
              customList: List<CustomData>.from(json['customData'].map((e)=> CustomData.fromJson(e))))
        ;
  Map<String, dynamic> toJson() => { "data": data, "customData": customData, "customList": customList };
}
```
