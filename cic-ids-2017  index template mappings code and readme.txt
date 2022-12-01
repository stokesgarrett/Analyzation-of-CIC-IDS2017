On elastic, go to dev tools, and in the console paste the code below
once pasted click green arrow to the right of PUT line
after it should say ackowledged true, which you can then upload csv file from
generatedlabelflows file, and it should be read

PUT /_index_template/cic-ids-2017
   {
        "index_patterns": [
          "cicids-header*"
        ],
        "template": {
          "mappings": {
            "_routing": {
              "required": false
            },
            "numeric_detection": false,
            "dynamic_date_formats": [
              "strict_date_optional_time",
              "yyyy/MM/dd HH:mm:ss Z||yyyy/MM/dd Z",
              "strict_date_time",
              "basic_date_time",
              "date_hour_minute",
              "date_hour_minute_second",
              "basic_ordinal_date_time"
            ],
            "dynamic": true,
            "_source": {
              "excludes": [],
              "includes": [],
              "enabled": true
            },
            "dynamic_templates": [],
            "date_detection": true,
            "properties": {
              "Subflow Fwd Bytes": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd URG Flags": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Min Packet Length": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd IAT Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Destination Port": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Active Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Label": {
                "type": "keyword"
              },
              "PSH Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Idle Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd Avg Bytes/Bulk": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd IAT Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Flow IAT Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Packet Length Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Idle Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Subflow Bwd Packets": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Source IP": {
                "type": "ip"
              },
              "Fwd IAT Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Flow Bytes/s": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Bwd Packet Length Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Bwd Avg Packets/Bulk": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Average Packet Size": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Init_Win_bytes_backward": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "RST Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd Packets/s": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Fwd Packet Length Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd Packet Length Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Active Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Destination IP": {
                "type": "ip"
              },
              "act_data_pkt_fwd": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "FIN Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Avg Packets/Bulk": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "URG Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Source Port": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd Packet Length Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Packet Length Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd IAT Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Subflow Bwd Bytes": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Max Packet Length": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Active Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Init_Win_bytes_forward": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "min_seg_size_forward": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Total Backward Packets": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Total Length of Bwd Packets": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Avg Fwd Segment Size": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Flow ID": {
                "eager_global_ordinals": false,
                "norms": false,
                "index": true,
                "store": false,
                "type": "keyword",
                "index_options": "docs",
                "split_queries_on_whitespace": false,
                "doc_values": true
              },
              "Fwd IAT Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "SYN Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Active Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Avg Bulk Rate": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "ECE Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Idle Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Timestamp": {
                "eager_global_ordinals": false,
                "index_phrases": false,
                "fielddata": false,
                "norms": true,
                "index": true,
                "store": false,
                "type": "text",
                "fields": {
                  "Timestamp": {
                    "index": true,
                    "ignore_malformed": false,
                    "store": false,
                    "type": "date",
                    "doc_values": true
                  }
                },
                "index_options": "positions"
              },
              "Fwd Avg Bytes/Bulk": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Flow IAT Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Total Length of Fwd Packets": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "ACK Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Flow IAT Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Flow Packets/s": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Bwd Header Length": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Idle Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Total Fwd Packets": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd IAT Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Protocol": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd Packet Length Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Flow IAT Min": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Avg Bwd Segment Size": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Fwd IAT Total": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd IAT Total": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Packet Length Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Fwd PSH Flags": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Packets/s": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Packet Length Variance": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Packet Length Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Bwd IAT Max": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd PSH Flags": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd IAT Mean": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Flow Duration": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd URG Flags": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "CWE Flag Count": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Fwd Header Length": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Packet Length Std": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "double",
                "doc_values": true
              },
              "Subflow Fwd Packets": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Bwd Avg Bulk Rate": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              },
              "Down/Up Ratio": {
                "coerce": true,
                "index": true,
                "ignore_malformed": false,
                "store": false,
                "type": "long",
                "doc_values": true
              }
            }
          }
        },
        "composed_of": []
      }
    }
  ]