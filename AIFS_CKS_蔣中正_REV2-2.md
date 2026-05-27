# AIFS v1.7.0 · Chiang Kai-shek（蔣中正）
# LOCK_ID : AIFS_LOCK_CKS_REV3
# Tier    : T1.8 | BL: L2 | Date: 2026-05-26
# Source  : historical collage + Wikimedia + 國家文化記憶庫 side profile (semi-measured)
# Fidelity: ~78%

---

## [UNIT] AU Anchors

```
HA1 = IPD = 1.000 AU  (92px)
HA2 = ICD / IPD = 0.64
HA3 = NW  / IPD = 0.72
OCD_check: ICD(0.64) + 2×EL(0.28) = 1.20 | OCD_Δ=0.03 ✅
```

---

## [LM] 15-Point Landmark

```
L01(-0.500, 0.000)  L02(+0.500, 0.000)  [fixed: pupil]
L03(-0.320, 0.010)  L04(+0.320, 0.010)  [med_cant]
L05(-0.610, 0.000)  L06(+0.610, 0.000)  [lat_cant]
L07( 0.000,-0.360)                       [nasion]
L08( 0.000, 0.340)                       [subnasale]
L09(-0.350, 0.360)  L10(+0.350, 0.360)  [alar]
L11( 0.000, 0.570)                       [labiale_sup]
L12(-0.410, 0.600)  L13(+0.410, 0.600)  [cheilion]
L14(-0.570, 1.030)                       [gonion_L]  ← updated jaw=1.19
L15( 0.000, 1.260)                       [menton]

2.5D : partial  (Z semi-measured from side profile data)

Validation:
  L03-L04 = 0.640 ✅ (ICD±0.02)
  L09-L10 = 0.700 ⚠️ (NW=0.72→Δ0.02 borderline)
  L12-L13 = 0.820 ✅ (MW±0.03)
  L07-L08 = 0.700 ✅ (MFH±0.03)
```

---

## [DB] COMPACT_DB

```
[AIFS_LOCK_CKS_REV3]|T1.8|L2|2026-05-26
HA|92px|ICD=0.64|NW=0.72|OCD_Δ=0.03|✅
G1|oval|up=norm|mid=long|low=short-norm
G2|monolid-tapered|tilt=-1°|fat=0.12|EL=0.28|ICD=0.64
G3|round_tip|br=med-high|NW=0.72|nla=92°|proj=mod
G4|1:1.42|MW=0.82|phil=0.15|corner=+1°
G5|narrow-round-soft_chin|jaw=1.19|jawA=126°|def=soft-narrow
G6|FW=1.33|zyg=mid_flat|cheek=flat
G7|feat=[bald_dome:lock,high_forehead:lock,monolid_small_eye:lock,thin_lip:lock,narrow_jaw:lock,high_nasal_bridge:lock,flattened_midface:lock]|asym=low|skin=est|glass=none
G8|M|W=1.45|D=1.20|fore=prom-round|orb=avg-slight_recessed|zygAR=0.41|mandD=0.17|chin=narrow-mod-proj
G9|LM|6/12semi|nas=Z0.02|ntip=Z0.22|sub=Z0.09|orbL=Z-0.05|orbR=Z-0.05|glab=Z0.11|ment=Z0.14|gon=Z0.06|pog=Z0.15|zygL=Z0.06|zygR=Z0.06|front=Z-0.16
LM|part|2.5D=partial|03=-0.32,0.01|04=0.32,0.01|05=-0.61,0.00|06=0.61,0.00|07=0,-0.36|08=0,0.34|09=-0.35,0.36|10=0.35,0.36|11=0,0.57|12=-0.41,0.60|13=0.41,0.60|14=-0.57,1.03|15=0,1.26
ML|low_est|mcl=0.18|mcd=0.06|mwd=0.09|jaw=0.24|esq=0.05|eo=0.03|br=0.04|bf=0.03|cp=0.09|nf=0.03|jw=0.05
MPIF|partial-high|P1_Z=0.22|P2_Z=0.09|P3_Z=0|P4_Z=-0.05|P5_Z=___|parallax=no
RL|OB🔴|NA🔴|MA🔴|MF🟡|OR🟡|UF🟢
COV|78%|ang=14/32|lit=7/20|3D=F✅/45⚠️/90⚠️|G9=6/12
BL|L2|jaw=1.10|FW=1.24|NW=0.68|tipΔ=0.00|eyeΔ=0.00
ANTI|no_eye_enlarge no_double_eyelid no_v_shape no_sharp_jaw no_high_zygoma no_flat_face no_nose_tip_overprojection no_skull_exaggeration no_deep_orbit_exaggerate no_bald_highlight_bias no_heroic_projection no_military_jaw no_strong_mandible
PRI|1=calibrated_bilateral_90°+12%|2=consistent_focal_length+8%|3=expression_set+7%
```

---

## [ML] Muscle Limits

```
conf = low_est  (neutral-only; no expression data)

mcl = 0.18   mcd = 0.06   mwd = 0.09   jaw = 0.24
esq = 0.05   eo  = 0.03   br  = 0.04   bf  = 0.03
cp  = 0.09   nf  = 0.03   jw  = 0.05

ML_Z_derived:
  jaw_Z  = 0.24 × 0.25 = 0.060
  cp_Z   = 0.09 × 0.40 = 0.036
  mcl_Z  = 0.18 × 0.25 = 0.045
  bf_Z   = 0.03 × 0.25 = 0.008
  br_Z   = 0.04 × 0.20 = 0.008
  eo_Z   = 0.03 × 0.12 = 0.004

⚠️ low_est: mcl/mwd/jaw/cp confidence limited — no open smile or speech frames
```

---

## [G9] Sparse Skeleton Coordinates

```
# Z=0: pupil plane. Z+: toward viewer. Z−: away. All AU.
# conf: measured | semi_measured | est | N_A

nasion:       X= 0.000   Y=-0.360   Z=+0.02   conf=semi_measured
nose_tip:     X= 0.000   Y= 0.220   Z=+0.22   conf=semi_measured
subnasale:    X= 0.000   Y= 0.340   Z=+0.09   conf=semi_measured
orbital_L:    X=-0.500   Y= 0.000   Z=-0.05   conf=semi_measured
orbital_R:    X=+0.500   Y= 0.000   Z=-0.05   conf=semi_measured
glabella:     X= 0.000   Y=-0.520   Z=+0.11   conf=est
menton:       X= 0.000   Y= 1.260   Z=+0.14   conf=semi_measured
gonion_L:     X=-0.595   Y= 1.030   Z=+0.06   conf=est
pogonion:     X= 0.000   Y= 1.100   Z=+0.15   conf=semi_measured
zygomatic_L:  X=-0.665   Y= 0.200   Z=+0.06   conf=semi_measured
zygomatic_R:  X=+0.665   Y= 0.200   Z=+0.06   conf=semi_measured
frontal_boss: X= 0.000   Y=-0.700   Z=-0.16   conf=est

G9_conf             = LM  (6/12 semi-measured)
landmark_2.5D_ready = partial
⚠️ single-side semi-profile; bilateral calibration pending
```

---

## [MPIF] Multi-Plane Identity Field

```
# Parallax formula: Δx = Z_plane × tan(θ)

P1_foreground  Z>+0.20 : nose_tip(0.22)                               drift🔴
P2_midface Z+0.05~+0.20: subnasale(0.09) glabella(0.11)
                          menton(0.14) pogonion(0.15)
                          zygomatic_L/R(0.06) gonion(0.06)            drift🟡
P3_orbital     Z≈0     : L01/L02 nasion(0.02)                         drift🔴(IPD abs)
P4_recessed Z-0.05~-0.20: orbital_L/R(-0.05) frontal_boss(-0.16)     drift🟡
P5_cranial     Z<-0.20 : occipital=___                                 drift🟢

MPIF_ready          = partial-high
parallax_calculable = no  (bilateral calibration needed)
VC_range            = ±30°

# Note vs REV2: P2 thinner (midface flatter), P4 shallower (orbital not deep-set)
```

---

## [DEPTH_CONF] Z-Axis Confidence Map

```
# status: semi_measured | inferred | unresolved
# source: 國家文化記憶庫 side + 1930 studio half-profile + official portraits

nose_tip.Z   = semi_measured  | Z=+0.22 | ±0.05
menton.Z     = semi_measured  | Z=+0.14 | ±0.05
subnasale.Z  = semi_measured  | Z=+0.09 | ±0.04
orbital.Z    = semi_measured  | Z=-0.05 | ±0.03
pogonion.Z   = semi_measured  | Z=+0.15 | ±0.05
zyg.Z        = semi_measured  | Z=+0.06 | ±0.04
nasion.Z     = semi_measured  | Z=+0.02 | ±0.04
glabella.Z   = inferred       | Z=+0.11 | ±0.06
gonion.Z     = inferred       | Z=+0.06 | ±0.05
skull_D      = inferred       | D= 1.20 | ±0.08
occipital.Z  = unresolved     | Z=___
cranial_arc  = moderate_round | conf=low

# Confidence propagation:
#   orbital.Z(semi) → MPIF P4 weight = medium (not high)
#   skull_D(inferred) → G8_D hard_lock = no
#   occipital(unresolved) → P5 = shell only
```

---

## [AGE] Age Layer

```
# Separates bone_static from soft_tissue_aging

bone_static:
  skull_W    = high    (stable across all ages)
  ICD        = high
  jawA       = high
  NW         = high
  LM_XY      = high

soft_tissue_aging:
  midface_fat_loss    = high     (aging hollow ≠ flat bone structure)
  orbital_hollow_age  = high     (老年陰影 ≠ 骨性深眼窩)
  jaw_softening_age   = medium
  temporal_hollowing  = medium
  cheek_flattening    = medium   (aging + naturally flat)
  nasolabial_aging    = light

target_bone_age     = ~30-45    (骨相基準年齡)
soft_tissue_var     = high      (體脂差異大)

⚠️ Do not lock orbital_depth or mandD from aged photos without correction
```

---

## [OPTICS] Lens Profile

```
# Lens contamination affects: jaw_width | nose_proj | forehead | cranial_W

1930_studio    : lens=probable_50mm  | compression=moderate | bias=jaw_narrow+nose_flat
1955_official  : lens=probable_85mm  | compression=low      | bias=minimal
wartime_press  : lens=unknown_wide   | compression=unknown  | bias=unknown

lens_bias_correction   = pending
AU_integrity           = medium  (lens contamination present)
weighted_geometry_ready = no

# Implication: jaw/FW/skull_W values carry ±0.05 lens uncertainty
```

---

## [SOFT_TISSUE]

```
# Features present that are NOT bone structure

temporal_loss       = present   (aging; temporal_W may read narrower than bone)
cheek_flattening    = present   (aging + naturally low zyg_proj)
orbital_shadowing   = present   (aging hollow; NOT deep-set bone → ANTI: no_deep_orbit_exaggerate)
nasolabial_aging    = light
jaw_softening       = present   (soft_thin_mandible; NOT military projection)
bald_highlight_bias = present   (禿頭高光 → skull_D overestimation risk → ANTI: no_bald_highlight_bias)

# Rule: separate before locking G8_D | mandD | orb_depth
```

---

## [AB] AI Boundary

```
LOCKED:
  geometry:
    IPD  = 1.000 abs
    ICD  = 0.64 ±0.03    → [0.61, 0.67]
    NW   ≥ 0.68          (BL L2 floor)
    jaw  ≥ 1.10          (BL L2 floor)
    G9 X,Y = all coords above
  depth:
    nose_tip.Z = 0.22 ±0.05   → [0.17, 0.27]
    orbital.Z  =-0.05 ±0.03   → [-0.08,-0.02]
    menton.Z   = 0.14 ±0.05   (neutral; expr→Z_eff)
    zygomatic.Z= 0.06          (neutral; expr→Z_eff)
    glabella.Z = 0.11          (neutral; expr→Z_eff)
  expr_Z_rule:
    G9_Z = neutral_Z + EXP_DELTA_Z  (ExprLib Z_ratio × ML_Z_derived)
  topology:
    L01-L06 (X,Y) locked
    canthal_tilt = -1° (dir locked)
    eyelid = monolid-tapered (locked)
    fat = 0.12 (<0.3; topology locked)
    G7_lock×7: bald_dome high_forehead monolid_small_eye
               thin_lip narrow_jaw high_nasal_bridge flattened_midface

FREE:
  surface:  pore/skin texture | lighting/shadow | makeup | color tone
  micro:    fine wrinkles | lash/brow detail | lip texture
  style:    photo vs painterly | bokeh | color grade | beauty within BL
```

---

## [VC] View Constraint

```
effective : horiz±30° | vert±15° | roll±10°  → full MPIF constraints active
marginal  : horiz 30–50° → generate + tag identity_confidence:marginal
out       : horiz>50° → ⚠️ identity guarantee void
GEN:ANGLE policy: in_range=normal | marginal=warn+generate | out=⚠️prompt user
```

---

## [RL] Region Lock Rules (person values)

```
OB🔴: IPD=1.000abs | ICD=0.64±0.03 | canthal_tilt=-1°(dir_locked) | eyelid=monolid-tapered(locked) | fat=0.12(locked) | EL=0.28±0.03 | eye_h≤+0.00
NA🔴: NW≥0.68 | bridge=med-high±0.03 | tip=round(locked) | nla=92°±5° | proj≤+0.00
MA🔴: jaw≥1.10 | jawA=126°±5° | chin=narrow-round-soft(locked) | mandD=0.17±0.08→[0.09,0.25] | def=soft-narrow(locked)
MF🟡: zyg=mid_flat(locked) | FW≥1.24 | zyg_proj±0.04(semi)
OR🟡: phil=0.15±0.03 | lip_ratio=1:1.42±0.10 | MW=0.82±0.05
UF🟢: temporal_W±0.05 | fore=prom-round(locked)
```

---

## [BL] Beauty Hard Limits — Level 2

```
jaw_floor   = 1.19 × 0.92 = 1.095  → ≥1.10
FW_floor    = 1.33 × 0.93 = 1.237  → ≥1.24
NW_floor    = 0.72 × 0.95 = 0.684  → ≥0.68
tip_Δceil   = +0.00
eye_h_Δceil = +0.00
```

---

## [COV] Coverage Matrix

```
# ✅direct ⚠️estimated/semi ❌none
# Angle × Expr (32 cells):
  front/neutral=✅  front/serious=✅  front/smile_s=⚠️  front/smile_o=❌
  15°/neutral=✅    15°/serious=⚠️   others=❌
  45°/neutral=⚠️   45°/serious=⚠️   others=❌
  90°/neutral=⚠️   90°/others=❌    (semi-profile; not calibrated bilateral)

# Light × Angle (20 cells):
  even_nat/front=✅    even_nat/15°=✅    even_nat/45°=⚠️   even_nat/90°=⚠️
  indoor_warm/front=✅  indoor_warm/15°=⚠️ others=❌
  side_light/front=⚠️  others=❌
  indoor_white=❌       nat_shade=❌

# 3D coverage:
  frontal_est=✅   side45_zygAR=⚠️   profile90=⚠️(semi; not calibrated)

ang  = 14/32
lit  = 7/20
G9   = 6/12 semi-measured
total= ~78%
```

---

## [TIER] Data Status

```
Current : T1.8 (~78%)
  have  : neutral_front ✅ | 45°⚠️ | 90°semi⚠️ | smile_o_front❌ | 3_lights partial
          side_profile semi-measured (single-side, not bilateral)

→ T2 needs (+12%):
  calibrated bilateral 90° (required v1.7) → G9 measured Z full
  consistent focal length → resolve AU lens contamination
  neutral_15° + laugh+surprise_front + side_light+indoor

→ T3 needs (+10% from T2):
  24-angle grid | 5 lights × front+45° | speaking_frames
  45°L+45°R bilateral | tilt_up+down
```

---

## [LOCK] Phase 3 Lock Vector

```
cranial_lock:
  skull_W=1.45±0.08    → [1.37,1.53]
  skull_D=1.20±0.08    → [1.12,1.28]  hard_lock=no (inferred)
  fore=prom-round(locked)
  orb=avg-slight_recessed(locked)
  zygAR=0.41±0.04      → [0.37,0.45]
  mandD=0.17±0.08      → [0.09,0.25]
  chin=narrow-mod-proj(locked)

LM_lock:
  L03-L04 = 0.64±0.02
  L09-L10 = 0.72±0.02
  L14_x   ≥ 1.10 (jaw floor)
  L15     = 1.26±0.04  → [1.22,1.30]
  2.5D: partial (6pt Z semi-measured; remaining est)

ML_lock:
  mcl=0.18 mcd=0.06 mwd=0.09 jaw=0.24
  esq=0.05 eo=0.03  br=0.04  bf=0.03
  cp=0.09  nf=0.03  jw=0.05  conf=low_est

ML_Z_derived:
  jaw_Z=0.060 cp_Z=0.036 mcl_Z=0.045
  bf_Z=0.008  br_Z=0.008  eo_Z=0.004

G9_lock:
  nose_tip.Z =+0.22±0.05   menton.Z =+0.14±0.05   orbital.Z=-0.05±0.03
  nasion.Z   =+0.02±0.04   glabella.Z=+0.11±0.06   zyg.Z    =+0.06±0.04
  hard_lock=6semi_measured  soft_lock=6est  G9_lock_active=partial

MPIF_lock:
  P1_Z_ref=0.22  P2_Z_ref=0.09  P3_Z_ref=0.000
  P4_Z_ref=-0.05 P5_Z_ref=___
```

---

## [GEN] Phase 4 Prompt Template

```
realistic photo of a [age]-year-old East Asian male,
[OB🔴] eye spacing 0.64 AU, outer corners -1° (slightly downward), monolid-tapered eyelids,
        minimal under-eye fat (0.12), eye width 0.28 AU,
[NA🔴] nose width 0.72 AU, med-high nasal bridge, nasolabial 92°, round moderate tip,
        nose tip protrudes 0.22 AU from eye plane,
[MA🔴] jaw 1.19 AU wide, jaw angle 126°, soft-narrow jawline, narrow-round-soft chin,
        chin projects 0.14 AU forward, skull depth 1.20 AU,
[MF🟡] face width 1.33 AU, mid-flat cheekbones (not prominent), flat cheeks,
        flattened midface structure,
[G8]   skull width 1.45 AU, prominent-round forehead, avg-slightly-recessed orbital depth,
        eye sockets recessed 0.05 AU (subtle, not deep-set),
[G7]   bald dome skull, high forehead, thin lips, narrow soft jaw, high nasal bridge
[SCENE] [lighting] [angle] 85mm photorealistic sharp focus,
[ANTI] no V-shaped jaw, jaw minimum 1.10 AU, no eye enlargement, no double eyelid,
       no nose narrowing, no prominent cheekbones, no deep-set eyes, no military jaw,
       no heroic projection, no strong mandible, no skull depth exaggeration,
       bald highlight is not skull depth, lighting shadow is not facial structure,
       no nose tip overprojection

# Angle variant (parallax pending bilateral calibration):
# [AIFS:GEN:ANGLE θ] nose shifts [0.22×tan(θ)] AU | chin shifts [0.14×tan(θ)] AU | eye width×cos(θ)
# identity_confidence: marginal at 30–50° | void >50°
```

---

## [EXPR] ExprLib Fields

```
expr_fields : mcl×0.18 | mcd×0.06 | mwd×0.09 | jaw×0.24 | esq×0.05 | eo×0.03
              br×0.04  | bf×0.03  | cp×0.09  | nf×0.03  | jw×0.05
Z_fields    : jaw_Z×0.060 | cp_Z×0.036 | mcl_Z×0.045 | bf_Z×0.008 | br_Z×0.008 | eo_Z×0.004
soft_fields : jaw_tension[0-1] | brow_tension[-1~+1] | lip_pressure[0-1] | eye_wet[0-1] | asym[-1~+1]
conf        : low_est (upgrade requires: open_smile + jaw_tension + speech frames)
```

---

## [VALID] Phase 5 Thresholds

```
T1: IPD_Δ=0.00abs | ICD∈[0.61,0.67] | NW∈[0.68,0.77]
T2: OB(tilt±2°_no_dir_reversal | EL∈[0.25,0.31] | eye_h≤+0.00)
    NA(bridge=med-high±0.03 | tip=round | proj≤+0.00)
    MA(jaw≥1.10 | angle∈[121°,131°] | mandD∈[0.09,0.25])
    MF(FW≥1.24→warn_only)
T3: L03/04_Δ≤±0.03(ref=±0.320) | L09/10_Δ≤±0.03(ref=±0.350) | L14_x≥1.10 | L15_Δ≤±0.04(ref=1.260)
T4: ExprLib_ratio≤1.0→auto_pass | manual_delta≤ML
T5: eyelid=monolid-tapered ✓ | G7_lock×7 visible ✓ | flattened_midface ✓
T6: [MPIF partial-high; bilateral pending]
    nose_tip_Δ≤±0.04 vs 0.22×tan(θ)
    menton_Δ≤±0.05 vs 0.14×tan(θ)
    IPD_persp_Δ≤±0.03 vs cos(θ)
    skip if angle=0°

Order: T1→T2→T3→T4→T5→T6. T1_fail=stop. ≥3_fails→lower_BL or add_photos.
```

---

## [CORRECT] Phase 6 Drift Fix

```
cranial_3D_drift     → reinforce: skull_W=1.45 skull_D=1.20 fore=prom-round jawA=126° mandD=0.17
                        neg: skull distortion, heroic projection, strong mandible
orbital_drift        → reinforce: ICD=0.64 EL=0.28 tilt=-1° monolid-tapered fat=0.12
                        neg: deep-set eyes, military brow ridge, sunken orbit
mandibular_drift     → reinforce: jaw=1.19 floor=1.10 def=soft-narrow
                        neg: strong jaw, military chin, V-shape
nasal_drift          → reinforce: NW=0.72 bridge=med-high tip=round-moderate
midface_drift        → reinforce: zyg=mid_flat cheek=flat flattened_midface
shadow_misread       → prompt+: "lighting shadow is not facial structure"
                        neg: sunken cheek, shadow-defined jawline, bald highlight as skull depth
aging_misread        → prompt+: "orbital hollow is aging soft tissue, not bone structure"
                        neg: deep-set eyes from aging shadow
expr_ratio_drift     → lower ExprLib intensity: high→medium→low
G9_geometry_drift    → [T6] prompt+: "nose protrudes 0.22 AU | chin 0.14 AU | orbit recessed 0.05 AU | at θ° nose shifts [0.22×tan(θ)] AU"
                        neg: flat face, no depth, 2D projection
view_constraint_viol → angle>30°: lower or tag identity_confidence:low
```

---

## [SIDE] Side View Protocol — Status

```
Status       : semi-executed (single-side, not bilateral calibrated)
Source       : 國家文化記憶庫 side profile + 1930 studio half-profile
G9_upgrade   : 2/12meas → 6/12semi_measured (+17% fidelity)

Completed:
  Z-extract  : 6 points semi-measured from side profiles ✅
  Z-validate :
    nose_tip.Z=0.22 ∈[+0.15,+0.45] ✅
    glabella.Z=0.11 ∈[+0.05,+0.25] ✅
    menton.Z  =0.14 ∈[+0.05,+0.35] ✅
    orbital.Z =-0.05 ∈[-0.05,-0.20] ⚠️ borderline (shallow)
    nasion.Z  =0.02 ∈[-0.05,+0.10] ✅
  G8 upgrade : mandD←menton.Z(0.14) | skulD revised to 1.20
  CROSSCHECK : G6_FW(1.33) vs G8_skulW(1.45) ✅ | G5_jawA(126°) vs MA_lock ✅

Pending:
  Step bilateral: left+right 90° → resolve single-side bias
  Step lens_norm: focal length normalization
  Step LM 2.5D full: 15pt Z lock
  Step MPIF parallax: parallax_calculable→yes
  Step P5: occipital fill
```

---

## [REPORT]

```
═══════════════════════════════════════════════════════
  AIFS v1.7 · Chiang Kai-shek（蔣中正）REV3
═══════════════════════════════════════════════════════
LOCK_ID        : AIFS_LOCK_CKS_REV3
資料等級       : Tier 1.8 / 3
照片數量       : ≥12（multi-source + side profile semi-measured）

══ 錨點基準層 ══════════════════════════════════════════
  IPD: 92px=1.000AU ✅ | ICD:0.64AU | NW:0.72AU | OCD:✅Δ=0.03 | LM:13pt⚠️ | 2.5D:partial

══ G8 頭骨立體層 ════════════════════════════════════════
  W=1.45AU[M] | D=1.20AU[inferred] | fore=prom-round | orb=avg-slight_recessed
  zygAR=0.41[semi] | mandD=0.17AU[semi] | chin=narrow-mod-proj

══ G9 稀疏骨架座標 ═══════════════════════════════════════
  [LM] | 6/12 semi-measured
  ntip.Z=+0.22[semi] | nas.Z=+0.02[semi] | ment.Z=+0.14[semi]
  orb.Z=-0.05[semi]  | glab.Z=+0.11[est] | zyg.Z=+0.06[semi]

══ MPIF 多平面身份場 ═════════════════════════════════════
  P1(Z>+0.20)       = nose_tip(0.22)
  P2(Z+0.05~+0.20)  = subnasale(0.09) glabella(0.11) menton(0.14) pogonion(0.15) zyg/gonion(0.06)
  P3(Z≈0)           = L01/L02 nasion(0.02)
  P4(Z-0.05~-0.20)  = orbital(-0.05) frontal_boss(-0.16)
  P5(Z<-0.20)       = occipital(___)
  ready=partial-high | parallax=no | VC_range=±30°

══ AI 決策邊界 ══════════════════════════════════════════
  locked: G9_XY+G9_Z+MPIF+LM_topology+monolid-tapered+fat(0.12)+G7_lock×7
  free:   texture/lighting/micro/style/beauty_within_BL

══ ML 肌肉物理上限 ══════════════════════════════════════
  [low_est] mcl=0.18 mcd=0.06 mwd=0.09 jaw=0.24 esq=0.05 eo=0.03 br=0.04 bf=0.03 cp=0.09 nf=0.03 jw=0.05

══ 分區漂移風險 ═════════════════════════════════════════
  🔴OB: ICD=0.64 tilt=-1° monolid-tapered fat=0.12
  🔴NA: NW=0.72 br=med-high tip=round-mod proj=mod
  🔴MA: jaw=1.19 angle=126° chin=narrow-round-soft soft-narrow
  🟡MF: FW=1.33 zyg=mid_flat cheek=flat flattened_midface
  🟡OR: MW=0.82 phil=0.15 corner=+1°
  🟢UF: fore=prom-round

══ 核心幾何（AU）════════════════════════════════════════
  G1: oval    up=norm  mid=long  low=short-norm
  G2: monolid-tapered  tilt=-1°  fat=0.12  EL=0.28  ICD=0.64
  G3: round_tip  br=med-high  NW=0.72  nla=92°  proj=mod
  G4: 1:1.42  MW=0.82  phil=0.15  corner=+1°
  G5: narrow-round-soft  jaw=1.19  jawA=126°  def=soft-narrow
  G6: FW=1.33  zyg=mid_flat  cheek=flat
  G7: feat=[bald_dome:lock, high_forehead:lock, monolid_small_eye:lock,
            thin_lip:lock, narrow_jaw:lock, high_nasal_bridge:lock, flattened_midface:lock]
      asym=low  skin=est  glass=none

══ 美顏設定 Level 2 ═════════════════════════════════════
  jaw≥1.10AU | FW≥1.24AU | NW≥0.68AU | tipΔ≤+0.00AU | eyeΔ≤+0.00AU

══ 覆蓋狀態 ═════════════════════════════════════════════
  [████▌░] ~78% | Tier1.8
  ang=14/32 | lit=7/20 | G8:F✅·45⚠️·90⚠️ | G9:6/12semi
  PRI: 1=bilateral_90°+12% | 2=focal_length_norm+8% | 3=expression_set+7%
═══════════════════════════════════════════════════════
```

---

## [VERSION]

```
EST_01 | 2026-05-26 | 初版（歷史拼圖照片）
REV1   | 2026-05-26 | shadow/skull bias 修正
REV2   | 2026-05-26 | Wikimedia 多來源交叉補強；全 section 展開
REV3   | 2026-05-26 | 側面資料補入（國家文化記憶庫 + 1930棚拍）
                      G9 2/12→6/12semi; orbital/menton/skull_D 下修
                      jaw/mandD/zyg/chin 修正; G7 +flattened_midface
                      ML.conf low_est; 新增 DEPTH_CONF/AGE/OPTICS/SOFT_TISSUE
```
