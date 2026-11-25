# MedDose Android project (prototype)

## What is included
- Native Android Studio project (Java, no third-party runtime libraries).
- Fully offline demonstration drug library stored in `app/src/main/assets/drugs.json`.
- Searchable drug list and hybrid drug pages (practical summary first, expanded information after).
- Gravity IV infusion calculator (mL/hour and drops/minute).
- Basic mg/kg dose arithmetic calculator.
- English-only interface.

## Important clinical limitation
This is a software prototype, NOT a validated drug formulary and NOT ready for clinical use. The bundled JSON contains only five demonstration records. Some deliberately omit dose values where a single universal regimen would be unsafe. All drug entries, dose ranges, age/gestation rules, preparation instructions, dilution, compatibility, renal/hepatic adjustments, and maximum doses must be researched, independently verified, dated, and clinically reviewed before patient-care use.

## Build
1. Install Android Studio.
2. Open this folder as an existing project.
3. Allow Gradle sync (Android Gradle Plugin 8.7.3; compile SDK 35).
4. Run on an Android device or emulator (minimum Android 6.0 / API 23).

## Planned next development stages
1. Agree on the initial high-priority drug list.
2. Build a structured, source-traceable formulary with adult, pediatric, and neonatal sections.
3. Add dose schedules by indication, age/gestational age, renal function, route, and maximum dose.
4. Add reconstitution/dilution, concentration, infusion, and unit-conversion calculators.
5. Add high-alert warnings, interaction/compatibility data, favorites, filters, and update/version controls.
6. Clinical review and validation by qualified pharmacists/physicians before release.

## Sources and licensing
BNF, Lexicomp, Micromedex, Medscape, Drugs.com, WHO, FDA, NICE, AAP, and recognized neonatal formularies can inform the research and verification workflow. Their proprietary content must not be copied into an offline app without the appropriate license or permission. The final database should cite the exact source, edition/version, access date, and relevant section for each monograph.

## Build a native Android APK using only your phone
1. Open GitHub in Chrome and sign in (create a free account if needed).
2. Create a new repository named MedDose.
3. Upload the project files from this folder, including `.github/workflows/android-build.yml`.
4. Open the repository's Actions tab and select **Build MedDose APK**. If needed, tap **Run workflow**.
5. When the run succeeds, open it and download the `MedDose-debug-apk` artifact.
6. Extract the artifact ZIP on your phone and install `app-debug.apk`. Allow installs from that browser/file manager if Android asks.

This is a debug APK for testing, not a signed public release. The bundled drug data remains a small demonstration dataset and is not clinically validated.
