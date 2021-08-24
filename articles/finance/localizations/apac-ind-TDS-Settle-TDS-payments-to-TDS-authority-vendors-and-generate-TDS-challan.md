---
title: Vypořádání plateb TDS prodejcům autorit TDS a generování challan TDS
description: Toto téma vysvětluje, jak vyrovnat platby daně odečtené u zdroje (TDS) prodejcům autorit TDS.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 19f41020c6e1db8b08c7f69a58d33852c730931447803e2e1e970b1c293b6acd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779391"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>Vypořádání plateb TDS prodejcům autorit TDS a generování challan TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vyrovnat platby daně odečtené u zdroje (TDS) prodejcům autorit TDS.

1. Přejděte na **Pohledávky \> Platby \> Deník plateb dodavatele**.

    [![Stránka deníku plateb dodavatelů.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Na stránce **Deník plateb dodavatele** vyberte **Nový** k vytvoření řádku deníku.
3. V poli **Účet** vyberte dodavatele oprávnění TDS, kterému chcete platby TDS zúčtovat.
4. Vyberte **Transakce vypořádání** k otevření stránky **Transakce vypořádání**, kde můžete zobrazit vypořádané transakce TDS pro dodavatele oprávnění TDS.

    Vypořádané transakce TDS za zúčtovací období se zobrazují následujícím způsobem:

    - Transakce TDS, kde je povaha kategorie posuzovaného **Společnost**, jsou zobrazeny jako jeden řádek transakce.
    - Transakce TDS, kde je povaha kategorie posuzovaného **HUF**, **Firma**, **Osoba**, **AOP**, **BOI**, **Obecní úřad** nebo **Ostatní**, jsou zobrazeny jako jeden řádek transakce.
    - Pole **Množství** zobrazuje celkovou částku TDS, která má být zaplacena prodejci autorit TDS.

5. Vyberte **Transakce srážkové daně** k zobrazení různých transakcí TDS, které jsou zahrnuty pro záznam vypořádání. Na této stránce můžete zobrazit rozdělení každé transakce TDS, která byla zahrnuta do procesu vypořádání pro období vypořádání.
6. Na kartě **Přehled** vyberte zaškrtávací políčko **Označit** pro transakce TDS k vypořádání s dodavatelem autorit TDS.

    Karta **Přehled** zobrazuje následující informace pro každou otevřenou transakci TDS:

    - **Datum** – Datum transakce TDS.
    - **Doklad** – Číslo dokladu.
    - **Zdroj** – Modul, ve kterém je zaúčtována transakce TDS.
    - **Prodejce/zákazník** – Číslo účtu prodejce nebo zákazníka, od kterého se odečte TDS.
    - **Jméno odpočtené osoby/strany** – Jméno prodejce nebo zákazníka, od kterého se odečte TDS.
    - **Povaha posuzovaného** – Povaha kategorie posuzovaného, do které odpočtená osoba patří.
    - **Částka** – Částka faktury, podle které byla TDS vypočítána.
    - **Výše daně** – Částka TDS, která byla vypočítána pro transakci.

    > [!NOTE]
    > Zrušte zaškrtnutí políčka **Označit** pro všechny transakce TDS, které by neměly být vypořádány prodejci autorit TDS.

    Na kartě **Všeobecné** je v poli **PAN** zobrazeno trvalé číslo účtu (PAN) příjemce. Pole **Datum** zobrazuje datum výpočtu TDS a pole **Hodnota** zobrazuje celkové procento, které bylo použito pro výpočet TDS.

7. Vyberte **Doklad** k zobrazení položek dokladu pro transakci TDS.
8. Zavřete stránku.
10. Vyberte **Složky srážkové daně** k otevření stránky **Složky srážkové daně**, kde si můžete prohlédnout TDS, která byla vypočítána podle daňové složky TDS pro konkrétní daňový kód TDS.

    Na kartě **Přehled** pole **Daňová složka** zobrazuje TDS daňovou složku, která byla použita pro transakci. Pole **Částka** pole zobrazuje částku TDS, která byla vypočtena pro daňovou složku TDS, v základní měně. Pole **Kumulovaná částka** zobrazuje celkovou částku TDS, která byla vypočtena pro daňovou složku TDS pro všechny vypořádané transakce.

    Na kartě **Částka** část **Výchozí měna** ukazuje částku TDS, která byla vypočtena pro daňovou složku TDS, ve výchozí měně. V části **Sekundární měna** je částka v sekundární měně.

11. Zavřete stránku **Složky srážkové daně**.
12. Na stránce **Otevřené úpravy transakcí** v poli **Množství** si všimněte si, že je aktualizována celková částka k vypořádání dodavateli autority TDS za zúčtovací období.
13. Chcete-li vypořádat transakce TDS různých období vypořádání TDS prodejci autorit TDS, zaškrtněte políčko **Označit** pro transakce.
14. Zavřete stránku **Otevřené úpravy transakcí**.

    > [!NOTE]
    > Pokud je pro vypořádání vybráno jen několik transakcí na stránce **Transakce srážkové daně**, celková částka TDS vybraných transakcí se aktualizuje v poli **Oprava** na stránce **Otevřené úpravy transakcí**. Částka opravy je aktualizována na řádku deníku na stránce **Doklad deníku** stránka a stránka **Otevřené úpravy transakcí** se zavře.

    Na stránce **Doklad deníku** pole **Debet** zobrazuje celkovou částku, která se má zaplatit prodejci autorit TDS.

15. Zadejte údaje offsetového účtu.

    > [!NOTE]
    > Pokud transakce TDS mají různá čísla daňových účtů (TAN), vytvářejí se řádky deníku za TAN na stránce **Doklad deníku**.

16. Na kartě **Poplatek za platbu** v poli **ID poplatku** vyberte ID poplatku, který má typ poplatku **Úrok** nebo **Ostatní** k účtování poplatku za zpoždění plateb provedených prodejci orgánu TDS.

    Na kartě **Daňové údaje** v části **Informace o společnosti** pole **Název** zobrazuje název společnosti. V části **Srážková daň** pole **Číslo daňového účtu (TAN)** ukazuje TAN, který je připojen k řádku transakce.

17. Proveďte ověření a zaúčtování deníku.
18. Vyberte **Srážková daň \> Informace challan** pro zadání údajů challan o transakci.

    Pole **Doklad** zobrazuje číslo dokladu transakce.
    
19. Zaškrtněte políčko **TDS uloženo zápisem do knihy**, pokud je částka TDS uložena pomocí zápisu do knihy.
20. Do pole **Číslo challan** zadejte číslo challan, které se používá k provedení platby prodejci orgánu TDS.
21. Do pole **Datum** zadejte datum challan.
22. V poli **Název banky** vyberte název banky, do které má být vložena částka TDS splatná dodavateli orgánu TDS. Toto pole obsahuje seznam všech bankovních účtů, které byly nastaveny pro dodavatele autorit TDS na adrese **Splatné účty \> Všichni prodejci \> Nastavení \> Bankovní účty**.
23. Do pole **Kód BSR** pole zadejte kód základní statistické návratnosti (BSR) banky.
24. Zavřete stránku.

### <a name="example"></a>Příklad

Období 04.01.2009 je zúčtováno pro skupinu komponent TDS **Pronájem** pomocí periodického procesu zúčtování TDS. Celková částka TDS 141 625,00 se zaúčtuje na účet autority dodavatele TDS pro období vypořádání TDS. Tuto částku můžete zobrazit v poli **Částka** na stránce **Otevřené úpravy transakcí** pro dodavatele autority TDS.

Pokud vyberete **Transakce srážkové daně**, k zobrazení různých transakcí TDS, které byly vypořádány za dané období, se zobrazí následující informace.

| Částka TDS |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Pro konkrétní částku Vyberte **Složky srážkové daně** k zobrazení TDS, která byla vypočítána podle daňové složky TDS pro konkrétní daňový kód TDS. V tomto příkladu vyberete **Složky srážkové daně** pro částku TDS 16 995,00. Zobrazí se částka daně, která byla vypočtena pro jednotlivé komponenty transakce.

| Daňová komponenta | Množství    | Akumulovaná částka |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Příplatek     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

Pokud jste vybrali pouze částky TDS 16 995,00, 22 660,00 a 28 325,00 pro vypořádání na stránce **Transakce srážkové daně**, celková částka pro vypořádání se zobrazuje jako **67 980,00** v poli **Oprava** na stránce **Otevřené úpravy transakcí**. Pokud je tato transakce označena k vypořádání a stránka **Otevřené úpravy transakcí** je zavřená, částka **67 980,00** je zobrazen v poli **Debet** na stránce **Doklad deníku**.

Nyní můžete zaúčtovat deník a vygenerovat TDS challan.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Úprava zálohových plateb, které jsou prováděny prodejcům autorit TDS

Chcete-li upravit zálohu, která byla provedena prodejci orgánu TDS, na skutečnou platbu, přejděte na **Závazky \> Prodejci \> Všichni prodejci \> Úpravy transakcí**. Pokud skutečná platba, která je provedena, přesahuje zálohu, jsou pro transakci vygenerována dvě challan čísla. V dotazu TDS se však zobrazuje pouze první číslo challan.
