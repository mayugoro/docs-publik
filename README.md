<details>
<summary><code>POST</code> <strong>/api/v1/sidompul/cek</strong> - Cek Info Dompul & Paket</summary>

Mengecek info detail nomer HP menggunakan multi provider.
Support : XL, Axis, Indosat, Tri.

**Headers**
```http
Authorization: Bearer <API_KEY_ANDA>
X-Client: <X_CLIENT_ANDA>
Content-Type: application/json
```

**Body**
```json
{
  "nomer": "081912345678", //wajib format 08xxx
  "x-pak": "<PUBLIC_API_KEY>"
}
```

**Response Success (200)**
```json
{
  "status": "success",
  "keterangan": "Berhasil cek dompul",
  "data": {
    "info_kartu": {
      "msisdn": "081912345678",
      "operator": "XL",
      "masa_aktif": "12 Oktober 2026",
      "masa_tenggang": "11 November 2026",
      "tenure": "3 Bulan"
    },
    "info_paket": [
      {
        "nama_paket": "Xtra Combo VIP",
        "tanggal_expire": "12 Oktober 2026",
        "kuota": [
          {
            "nama": "Kuota Utama",
            "sisa": "10.5 GB",
            "total": "15 GB",
            "persen": 70,
            "satuan": "GB",
            "tipe": "DATA"
          }
        ]
      }
    ]
  }
}
```
> ⚠️ **Note:** Nilai `X-PAK` adalah wajib, sebagai parameter pelindung agar permintaan bersumber asli dari anda, bukan spammer.
> **Best Regards:** `Mayugoro`
</details>
