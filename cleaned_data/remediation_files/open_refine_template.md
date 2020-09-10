**Prefix:**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body:**

```
<mods>

<identifier type="pid">{{cells["PID"].value}}</identifier>

<titleInfo><title>{{cells["title"].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells['namePart'].value), '', '<name'+ if(isBlank(cells['name.URI'].value), '', ' valueURI="' + cells['name.URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['namePart'].value + '</namePart>' + if(isBlank(cells['roleTerm'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['roleTerm'].value + '</roleTerm></role>') + '</name>')}}

<originInfo>
{{if(isBlank(cells["dateCreated"].value),'','<dateCreated>' + cells['dateCreated'].value + '</dateCreated>')}}
{{if(isBlank(cells["date_edtf"].value),'','<dateCreated encoding="edtf">' + cells['date_edtf'].value + '</dateCreated>')}}
{{if(isBlank(cells["dateRange_start"].value),'','<dateCreated encoding="edtf" point="start">' + cells['dateRange_start'].value + '</dateCreated>' + '<dateCreated encoding="edtf" point="end">' + cells['dateRange_end'].value + '</dateCreated>')}}
</originInfo>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><internetMediaType>{{cells['internetMediaType'].value}}</internetMediaType></physicalDescription>

{{if(isBlank(cells['subject_topic'].value), '', '<subject' + if(isBlank(cells['subject_topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '">') + '<topic>' + cells['subject_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.topic'].value), '', '<subject' + if(isBlank(cells['subject.topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.topic_URI'].value + '">') + '<topic>' + cells['subject.topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo_blanket'].value), '', '<subject' +  if(isBlank(cells['subject_geo_blanket_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject_geo_blanket_URI'].value + '">') + '<geographic>' + cells['subject_geo_blanket'].value + '</geographic>' + if(isBlank(cells['subject_geo_blanket_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_geo_blanket_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.0geographic'].value), '', '<subject' +  if(isBlank(cells['subject.0geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.0geographic_URI'].value + '">') + '<geographic>' + cells['subject.0geographic'].value + '</geographic>' + if(isBlank(cells['subject.0geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.0geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.1geographic'].value), '', '<subject' +  if(isBlank(cells['subject.1geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.1geographic_URI'].value + '">') + '<geographic>' + cells['subject.1geographic'].value + '</geographic>' + if(isBlank(cells['subject.1geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.1geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.2geographic'].value), '', '<subject' +  if(isBlank(cells['subject.2geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.2geographic_URI'].value + '">') + '<geographic>' + cells['subject.2geographic'].value + '</geographic>' + if(isBlank(cells['subject.2geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.2geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.3geographic'].value), '', '<subject' +  if(isBlank(cells['subject.3geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.3geographic_URI'].value + '">') + '<geographic>' + cells['subject.3geographic'].value + '</geographic>' + if(isBlank(cells['subject.3geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.3geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.4geographic'].value), '', '<subject' +  if(isBlank(cells['subject.4geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.4geographic_URI'].value + '">') + '<geographic>' + cells['subject.4geographic'].value + '</geographic>' + if(isBlank(cells['subject.4geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.4geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.5geographic'].value), '', '<subject' +  if(isBlank(cells['subject.5geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.5geographic_URI'].value + '">') + '<geographic>' + cells['subject.5geographic'].value + '</geographic>' + if(isBlank(cells['subject.5geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.5geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.6geographic'].value), '', '<subject' +  if(isBlank(cells['subject.6geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.6geographic_URI'].value + '">') + '<geographic>' + cells['subject.6geographic'].value + '</geographic>' + if(isBlank(cells['subject.6geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.6geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject.7geographic'].value), '', '<subject' +  if(isBlank(cells['subject.7geographic_URI'].value), '>',' authority="geonames" valueURI="' + cells['subject.7geographic_URI'].value + '">') + '<geographic>' + cells['subject.7geographic'].value + '</geographic>' + if(isBlank(cells['subject.7geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject.7geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

<recordInfo><recordContentSource valueURI="{{cells['source_URI'].value}}">{{cells['source'].value}}</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```



**Suffix:**

```
</modsCollection>
```

