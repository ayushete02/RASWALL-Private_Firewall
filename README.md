`qqqqqqqq`

```bash
loadmodule "http_client.so"
loadmodule "htable.so"
... 
modparam("htable", "htable", "ipban=>size=8;autoexpire=600;")
... 
if (!pike_check_req()) {
  xlog("L_ALERT","ALERT: pike blocking $rm from $fu (IP:$si:$sp)\n");
  $sht(ipban=>$si) = 1;
  http_client_query("http://localhost:8082/addip/$si", "$var(apinfo)");
  exit;
}
... 
event_route[htable:expired:ipban] {
  xlog("mytable record expired $shtrecord(key) => $shtrecord(value)\n");
  http_client_query("http://localhost:8082/removeip/$shtrecord(key)", "$var(apinfo)");
}
```

# qqqqqq
## ffffff
### ffgggfg

* ***fff***
- ddfff
