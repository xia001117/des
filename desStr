function a(e) {
    var t = new Array(),
      n = e.length,
      r = parseInt(n / 4),
      a = n % 4,
      i = 0;
    for (i = 0; i < r; i++) t[i] = o(e.substring(4 * i + 0, 4 * i + 4));
    return a > 0 && (t[i] = o(e.substring(4 * i + 0, n))), t;
  }
  function o(e) {
    var t = e.length,
      n = new Array(64);
    if (t < 4) {
      var r = 0,
        a = 0,
        o = 0,
        i = 0;
      for (r = 0; r < t; r++) {
        var s = e.charCodeAt(r);
        for (a = 0; a < 16; a++) {
          var c = 1,
            u = 0;
          for (u = 15; u > a; u--) c *= 2;
          n[16 * r + a] = parseInt(s / c) % 2;
        }
      }
      for (o = t; o < 4; o++) {
        s = 0;
        for (i = 0; i < 16; i++) {
          (c = 1), (u = 0);
          for (u = 15; u > i; u--) c *= 2;
          n[16 * o + i] = parseInt(s / c) % 2;
        }
      }
    } else
      for (r = 0; r < 4; r++) {
        s = e.charCodeAt(r);
        for (a = 0; a < 16; a++) {
          c = 1;
          for (u = 15; u > a; u--) c *= 2;
          n[16 * r + a] = parseInt(s / c) % 2;
        }
      }
    return n;
  }
  function i(e) {
    var t;
    switch (e) {
      case "0000":
        t = "0";
        break;
      case "0001":
        t = "1";
        break;
      case "0010":
        t = "2";
        break;
      case "0011":
        t = "3";
        break;
      case "0100":
        t = "4";
        break;
      case "0101":
        t = "5";
        break;
      case "0110":
        t = "6";
        break;
      case "0111":
        t = "7";
        break;
      case "1000":
        t = "8";
        break;
      case "1001":
        t = "9";
        break;
      case "1010":
        t = "A";
        break;
      case "1011":
        t = "B";
        break;
      case "1100":
        t = "C";
        break;
      case "1101":
        t = "D";
        break;
      case "1110":
        t = "E";
        break;
      case "1111":
        t = "F";
    }
    return t;
  }
  function s(e) {
    var t = "",
      n = 0,
      r = 0;
    for (n = 0; n < 16; n++) {
      var a = "";
      for (r = 0; r < 4; r++) a += e[4 * n + r];
      t += i(a);
    }
    return t;
  }
  function c(e, t) {
    var n = _(t),
      r = u(e),
      a = new Array(32),
      o = new Array(32),
      i = new Array(32),
      s = 0,
      c = 0,
      m = 0,
      y = 0,
      h = 0;
    for (m = 0; m < 32; m++) (a[m] = r[m]), (o[m] = r[32 + m]);
    for (s = 0; s < 16; s++) {
      for (c = 0; c < 32; c++) (i[c] = a[c]), (a[c] = o[c]);
      var g = new Array(48);
      for (y = 0; y < 48; y++) g[y] = n[s][y];
      var b = v(d(f(v(l(o), g))), i);
      for (h = 0; h < 32; h++) o[h] = b[h];
    }
    var T = new Array(64);
    for (s = 0; s < 32; s++) (T[s] = o[s]), (T[32 + s] = a[s]);
    return p(T);
  }
  function u(e) {
    var t = new Array(64),
      n = 0,
      r = 0,
      a = 0,
      o = 0,
      i = 0;
    for (n = 0, o = 1, i = 0; n < 4; n++, o += 2, i += 2)
      for (r = 7, a = 0; r >= 0; r--, a++)
        (t[8 * n + a] = e[8 * r + o]), (t[8 * n + a + 32] = e[8 * r + i]);
    return t;
  }
  function l(e) {
    var t = new Array(48),
      n = 0;
    for (n = 0; n < 8; n++)
      (t[6 * n + 0] = 0 == n ? e[31] : e[4 * n - 1]),
        (t[6 * n + 1] = e[4 * n + 0]),
        (t[6 * n + 2] = e[4 * n + 1]),
        (t[6 * n + 3] = e[4 * n + 2]),
        (t[6 * n + 4] = e[4 * n + 3]),
        (t[6 * n + 5] = 7 == n ? e[0] : e[4 * n + 4]);
    return t;
  }
  function v(e, t) {
    var n = new Array(e.length),
      r = 0;
    for (r = 0; r < e.length; r++) n[r] = e[r] ^ t[r];
    return n;
  }
  function f(e) {
    var t = new Array(32),
      n = "",
      r = [
        [14, 4, 13, 1, 2, 15, 11, 8, 3, 10, 6, 12, 5, 9, 0, 7],
        [0, 15, 7, 4, 14, 2, 13, 1, 10, 6, 12, 11, 9, 5, 3, 8],
        [4, 1, 14, 8, 13, 6, 2, 11, 15, 12, 9, 7, 3, 10, 5, 0],
        [15, 12, 8, 2, 4, 9, 1, 7, 5, 11, 3, 14, 10, 0, 6, 13],
      ],
      a = [
        [15, 1, 8, 14, 6, 11, 3, 4, 9, 7, 2, 13, 12, 0, 5, 10],
        [3, 13, 4, 7, 15, 2, 8, 14, 12, 0, 1, 10, 6, 9, 11, 5],
        [0, 14, 7, 11, 10, 4, 13, 1, 5, 8, 12, 6, 9, 3, 2, 15],
        [13, 8, 10, 1, 3, 15, 4, 2, 11, 6, 7, 12, 0, 5, 14, 9],
      ],
      o = [
        [10, 0, 9, 14, 6, 3, 15, 5, 1, 13, 12, 7, 11, 4, 2, 8],
        [13, 7, 0, 9, 3, 4, 6, 10, 2, 8, 5, 14, 12, 11, 15, 1],
        [13, 6, 4, 9, 8, 15, 3, 0, 11, 1, 2, 12, 5, 10, 14, 7],
        [1, 10, 13, 0, 6, 9, 8, 7, 4, 15, 14, 3, 11, 5, 2, 12],
      ],
      i = [
        [7, 13, 14, 3, 0, 6, 9, 10, 1, 2, 8, 5, 11, 12, 4, 15],
        [13, 8, 11, 5, 6, 15, 0, 3, 4, 7, 2, 12, 1, 10, 14, 9],
        [10, 6, 9, 0, 12, 11, 7, 13, 15, 1, 3, 14, 5, 2, 8, 4],
        [3, 15, 0, 6, 10, 1, 13, 8, 9, 4, 5, 11, 12, 7, 2, 14],
      ],
      s = [
        [2, 12, 4, 1, 7, 10, 11, 6, 8, 5, 3, 15, 13, 0, 14, 9],
        [14, 11, 2, 12, 4, 7, 13, 1, 5, 0, 15, 10, 3, 9, 8, 6],
        [4, 2, 1, 11, 10, 13, 7, 8, 15, 9, 12, 5, 6, 3, 0, 14],
        [11, 8, 12, 7, 1, 14, 2, 13, 6, 15, 0, 9, 10, 4, 5, 3],
      ],
      c = [
        [12, 1, 10, 15, 9, 2, 6, 8, 0, 13, 3, 4, 14, 7, 5, 11],
        [10, 15, 4, 2, 7, 12, 9, 5, 6, 1, 13, 14, 0, 11, 3, 8],
        [9, 14, 15, 5, 2, 8, 12, 3, 7, 0, 4, 10, 1, 13, 11, 6],
        [4, 3, 2, 12, 9, 5, 15, 10, 11, 14, 1, 7, 6, 0, 8, 13],
      ],
      u = [
        [4, 11, 2, 14, 15, 0, 8, 13, 3, 12, 9, 7, 5, 10, 6, 1],
        [13, 0, 11, 7, 4, 9, 1, 10, 14, 3, 5, 12, 2, 15, 8, 6],
        [1, 4, 11, 13, 12, 3, 7, 14, 10, 15, 6, 8, 0, 5, 9, 2],
        [6, 11, 13, 8, 1, 4, 10, 7, 9, 5, 0, 15, 14, 2, 3, 12],
      ],
      l = [
        [13, 2, 8, 4, 6, 15, 11, 1, 10, 9, 3, 14, 5, 0, 12, 7],
        [1, 15, 13, 8, 10, 3, 7, 4, 12, 5, 6, 11, 0, 14, 9, 2],
        [7, 11, 4, 1, 9, 12, 14, 2, 0, 6, 10, 13, 15, 3, 5, 8],
        [2, 1, 14, 7, 4, 10, 8, 13, 15, 12, 9, 0, 3, 5, 6, 11],
      ],
      v = 0;
    for (v = 0; v < 8; v++) {
      var f, d;
      switch (
        ((f = 2 * e[6 * v + 0] + e[6 * v + 5]),
        (d =
          2 * e[6 * v + 1] * 2 * 2 +
          2 * e[6 * v + 2] * 2 +
          2 * e[6 * v + 3] +
          e[6 * v + 4]),
        v)
      ) {
        case 0:
          n = m(r[f][d]);
          break;
        case 1:
          n = m(a[f][d]);
          break;
        case 2:
          n = m(o[f][d]);
          break;
        case 3:
          n = m(i[f][d]);
          break;
        case 4:
          n = m(s[f][d]);
          break;
        case 5:
          n = m(c[f][d]);
          break;
        case 6:
          n = m(u[f][d]);
          break;
        case 7:
          n = m(l[f][d]);
      }
      (t[4 * v + 0] = parseInt(n.substring(0, 1))),
        (t[4 * v + 1] = parseInt(n.substring(1, 2))),
        (t[4 * v + 2] = parseInt(n.substring(2, 3))),
        (t[4 * v + 3] = parseInt(n.substring(3, 4)));
    }
    return t;
  }
  function d(e) {
    var t = new Array(32);
    return (
      (t[0] = e[15]),
      (t[1] = e[6]),
      (t[2] = e[19]),
      (t[3] = e[20]),
      (t[4] = e[28]),
      (t[5] = e[11]),
      (t[6] = e[27]),
      (t[7] = e[16]),
      (t[8] = e[0]),
      (t[9] = e[14]),
      (t[10] = e[22]),
      (t[11] = e[25]),
      (t[12] = e[4]),
      (t[13] = e[17]),
      (t[14] = e[30]),
      (t[15] = e[9]),
      (t[16] = e[1]),
      (t[17] = e[7]),
      (t[18] = e[23]),
      (t[19] = e[13]),
      (t[20] = e[31]),
      (t[21] = e[26]),
      (t[22] = e[2]),
      (t[23] = e[8]),
      (t[24] = e[18]),
      (t[25] = e[12]),
      (t[26] = e[29]),
      (t[27] = e[5]),
      (t[28] = e[21]),
      (t[29] = e[10]),
      (t[30] = e[3]),
      (t[31] = e[24]),
      t
    );
  }
  function p(e) {
    var t = new Array(64);
    return (
      (t[0] = e[39]),
      (t[1] = e[7]),
      (t[2] = e[47]),
      (t[3] = e[15]),
      (t[4] = e[55]),
      (t[5] = e[23]),
      (t[6] = e[63]),
      (t[7] = e[31]),
      (t[8] = e[38]),
      (t[9] = e[6]),
      (t[10] = e[46]),
      (t[11] = e[14]),
      (t[12] = e[54]),
      (t[13] = e[22]),
      (t[14] = e[62]),
      (t[15] = e[30]),
      (t[16] = e[37]),
      (t[17] = e[5]),
      (t[18] = e[45]),
      (t[19] = e[13]),
      (t[20] = e[53]),
      (t[21] = e[21]),
      (t[22] = e[61]),
      (t[23] = e[29]),
      (t[24] = e[36]),
      (t[25] = e[4]),
      (t[26] = e[44]),
      (t[27] = e[12]),
      (t[28] = e[52]),
      (t[29] = e[20]),
      (t[30] = e[60]),
      (t[31] = e[28]),
      (t[32] = e[35]),
      (t[33] = e[3]),
      (t[34] = e[43]),
      (t[35] = e[11]),
      (t[36] = e[51]),
      (t[37] = e[19]),
      (t[38] = e[59]),
      (t[39] = e[27]),
      (t[40] = e[34]),
      (t[41] = e[2]),
      (t[42] = e[42]),
      (t[43] = e[10]),
      (t[44] = e[50]),
      (t[45] = e[18]),
      (t[46] = e[58]),
      (t[47] = e[26]),
      (t[48] = e[33]),
      (t[49] = e[1]),
      (t[50] = e[41]),
      (t[51] = e[9]),
      (t[52] = e[49]),
      (t[53] = e[17]),
      (t[54] = e[57]),
      (t[55] = e[25]),
      (t[56] = e[32]),
      (t[57] = e[0]),
      (t[58] = e[40]),
      (t[59] = e[8]),
      (t[60] = e[48]),
      (t[61] = e[16]),
      (t[62] = e[56]),
      (t[63] = e[24]),
      t
    );
  }
  function m(e) {
    var t = "";
    switch (e) {
      case 0:
        t = "0000";
        break;
      case 1:
        t = "0001";
        break;
      case 2:
        t = "0010";
        break;
      case 3:
        t = "0011";
        break;
      case 4:
        t = "0100";
        break;
      case 5:
        t = "0101";
        break;
      case 6:
        t = "0110";
        break;
      case 7:
        t = "0111";
        break;
      case 8:
        t = "1000";
        break;
      case 9:
        t = "1001";
        break;
      case 10:
        t = "1010";
        break;
      case 11:
        t = "1011";
        break;
      case 12:
        t = "1100";
        break;
      case 13:
        t = "1101";
        break;
      case 14:
        t = "1110";
        break;
      case 15:
        t = "1111";
    }
    return t;
  }
  function _(e) {
    var t = new Array(56),
      n = new Array();
    (n[0] = new Array()),
      (n[1] = new Array()),
      (n[2] = new Array()),
      (n[3] = new Array()),
      (n[4] = new Array()),
      (n[5] = new Array()),
      (n[6] = new Array()),
      (n[7] = new Array()),
      (n[8] = new Array()),
      (n[9] = new Array()),
      (n[10] = new Array()),
      (n[11] = new Array()),
      (n[12] = new Array()),
      (n[13] = new Array()),
      (n[14] = new Array()),
      (n[15] = new Array());
    var r = [1, 1, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 2, 1];
    for (a = 0; a < 7; a++)
      for (o = 0, i = 7; o < 8; o++, i--) t[8 * a + o] = e[8 * i + a];
    var a = 0,
      o = 0,
      i = 0,
      s = 0;
    for (a = 0; a < 16; a++) {
      var c = 0,
        u = 0;
      for (o = 0; o < r[a]; o++) {
        for (c = t[0], u = t[28], i = 0; i < 27; i++)
          (t[i] = t[i + 1]), (t[28 + i] = t[29 + i]);
        (t[27] = c), (t[55] = u);
      }
      var l = new Array(48);
      switch (
        ((l[0] = t[13]),
        (l[1] = t[16]),
        (l[2] = t[10]),
        (l[3] = t[23]),
        (l[4] = t[0]),
        (l[5] = t[4]),
        (l[6] = t[2]),
        (l[7] = t[27]),
        (l[8] = t[14]),
        (l[9] = t[5]),
        (l[10] = t[20]),
        (l[11] = t[9]),
        (l[12] = t[22]),
        (l[13] = t[18]),
        (l[14] = t[11]),
        (l[15] = t[3]),
        (l[16] = t[25]),
        (l[17] = t[7]),
        (l[18] = t[15]),
        (l[19] = t[6]),
        (l[20] = t[26]),
        (l[21] = t[19]),
        (l[22] = t[12]),
        (l[23] = t[1]),
        (l[24] = t[40]),
        (l[25] = t[51]),
        (l[26] = t[30]),
        (l[27] = t[36]),
        (l[28] = t[46]),
        (l[29] = t[54]),
        (l[30] = t[29]),
        (l[31] = t[39]),
        (l[32] = t[50]),
        (l[33] = t[44]),
        (l[34] = t[32]),
        (l[35] = t[47]),
        (l[36] = t[43]),
        (l[37] = t[48]),
        (l[38] = t[38]),
        (l[39] = t[55]),
        (l[40] = t[33]),
        (l[41] = t[52]),
        (l[42] = t[45]),
        (l[43] = t[41]),
        (l[44] = t[49]),
        (l[45] = t[35]),
        (l[46] = t[28]),
        (l[47] = t[31]),
        a)
      ) {
        case 0:
          for (s = 0; s < 48; s++) n[0][s] = l[s];
          break;
        case 1:
          for (s = 0; s < 48; s++) n[1][s] = l[s];
          break;
        case 2:
          for (s = 0; s < 48; s++) n[2][s] = l[s];
          break;
        case 3:
          for (s = 0; s < 48; s++) n[3][s] = l[s];
          break;
        case 4:
          for (s = 0; s < 48; s++) n[4][s] = l[s];
          break;
        case 5:
          for (s = 0; s < 48; s++) n[5][s] = l[s];
          break;
        case 6:
          for (s = 0; s < 48; s++) n[6][s] = l[s];
          break;
        case 7:
          for (s = 0; s < 48; s++) n[7][s] = l[s];
          break;
        case 8:
          for (s = 0; s < 48; s++) n[8][s] = l[s];
          break;
        case 9:
          for (s = 0; s < 48; s++) n[9][s] = l[s];
          break;
        case 10:
          for (s = 0; s < 48; s++) n[10][s] = l[s];
          break;
        case 11:
          for (s = 0; s < 48; s++) n[11][s] = l[s];
          break;
        case 12:
          for (s = 0; s < 48; s++) n[12][s] = l[s];
          break;
        case 13:
          for (s = 0; s < 48; s++) n[13][s] = l[s];
          break;
        case 14:
          for (s = 0; s < 48; s++) n[14][s] = l[s];
          break;
        case 15:
          for (s = 0; s < 48; s++) n[15][s] = l[s];
      }
    }
    return n;
  }
  function desStr(e, t = "0979ebb", n, r) {
    var i,
      u,
      l,
      v,
      f,
      d,
      p = e.length,
      m = "";
    null != t && "" != t && ((i = a(t)), (v = i.length));
    null != n && "" != n && ((u = a(n)), (f = u.length));
    null != r && "" != r && ((l = a(r)), (d = l.length));
    if (p > 0)
      if (p < 4) {
        var _ = o(e);
        if (
          null != t &&
          "" != t &&
          null != n &&
          "" != n &&
          null != r &&
          "" != r
        ) {
          for (S = _, y = 0; y < v; y++) S = c(S, i[y]);
          for (D = 0; D < f; D++) S = c(S, u[D]);
          for (N = 0; N < d; N++) S = c(S, l[N]);
          w = S;
        } else if (null != t && "" != t && null != n && "" != n) {
          for (S = _, y = 0; y < v; y++) S = c(S, i[y]);
          for (D = 0; D < f; D++) S = c(S, u[D]);
          w = S;
        } else if (null != t && "" != t) {
          var y = 0;
          for (S = _, y = 0; y < v; y++) S = c(S, i[y]);
          w = S;
        }
        m = s(w);
      } else {
        var h = parseInt(p / 4),
          g = p % 4,
          b = 0;
        for (b = 0; b < h; b++) {
          var T = o(e.substring(4 * b + 0, 4 * b + 4));
          if (
            null != t &&
            "" != t &&
            null != n &&
            "" != n &&
            null != r &&
            "" != r
          ) {
            for (S = T, y = 0; y < v; y++) S = c(S, i[y]);
            for (D = 0; D < f; D++) S = c(S, u[D]);
            for (N = 0; N < d; N++) S = c(S, l[N]);
            w = S;
          } else if (null != t && "" != t && null != n && "" != n) {
            for (S = T, y = 0; y < v; y++) S = c(S, i[y]);
            for (D = 0; D < f; D++) S = c(S, u[D]);
            w = S;
          } else if (null != t && "" != t) {
            for (S = T, y = 0; y < v; y++) S = c(S, i[y]);
            w = S;
          }
          m += s(w);
        }
        if (g > 0) {
          var w;
          T = o(e.substring(4 * h + 0, p));
          if (
            null != t &&
            "" != t &&
            null != n &&
            "" != n &&
            null != r &&
            "" != r
          ) {
            var N;
            for (S = T, y = 0; y < v; y++) S = c(S, i[y]);
            for (D = 0; D < f; D++) S = c(S, u[D]);
            for (N = 0; N < d; N++) S = c(S, l[N]);
            w = S;
          } else if (null != t && "" != t && null != n && "" != n) {
            var D;
            for (S = T, y = 0; y < v; y++) S = c(S, i[y]);
            for (D = 0; D < f; D++) S = c(S, u[D]);
            w = S;
          } else if (null != t && "" != t) {
            var S;
            for (S = T, y = 0; y < v; y++) S = c(S, i[y]);
            w = S;
          }
          m += s(w);
        }
      }
    return m;
  }
//导出
module.exports = desStr;
