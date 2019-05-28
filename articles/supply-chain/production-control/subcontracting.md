---
title: Subdodávka
description: Toto téma vás provede subdodávkami ve výrobě v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568376"
---
# <a name="subcontracting"></a>Subdodávka

[!include [banner](../includes/banner.md)]

Toto téma vás provede subdodávkami ve výrobě v aplikaci Microsoft Dynamics 365 for Finance and Operations. První část tohoto tématu popisuje nastavení dat. Druhá část vás provede kroky v této ukázce.

## <a name="target-audience"></a>Cílová skupina

V tomto tématu se naučíte, jak nastavit subdodávky ve výrobě. Budete používat existující data v právnické osobě HQUS k provedení základního nastavení toku aktivity subdodávky. Ukázková data v právnické osobě HQUS obsahují nastavení parametrů, které byly přednastaveny k podpoře kroků v ukázce. Přestože ukázka adresuje klíčové problémy a výzvy pro různé role, může ji dokončit správce systému.

## <a name="demo-scenario"></a>Scénář ukázky

V právnické osobě HQUS jsou vyráběny špičkové reproduktory. Během výrobního procesu procházejí reproduktory třemi následujícími operacemi.

- **Předběžné sestavení** – Skříň reproduktoru je sestavena. Materiál pro skříň je vydán ve skladu materiálu před zahájením operace.
- **Lakování** – Po sestavení skříně reproduktoru je třeba ji nalakovat. Tuto operaci provádí dodavatel (subdodavatel). Předběžně sestavená skříň reproduktoru je expedována subdodavateli k nátěru spolu s dvěma materiály.
- **Konečná úprava** – Poté, co je předběžně sestavená skříň reproduktoru nalakována subdodavatelem, vrátí se do právnické osoby HQUS, aby bylo dokončeno finální sestavení.

Následující obrázek znázorňuje tři operace a materiály, které tyto operace spotřebovávají.

![Předběžné sestavení lakování a operace dokončení, spolu se spotřebovávanými materiály.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Nastavení

Dříve než začnete s ukázkou, musíte nastavit data.

### <a name="set-up-the-finished-product"></a>Nastavení dokončeného produktu

Tento postup vás provede nastavením uvolněného produktu D8100, „Nalakovaná skříň.“

1. Vyberte **Řízení informací o produktech \> Produkty \> Uvolněné produkty** pro otevření stránky **Podrobnosti uvolněného produktu**.
2. V poli rychlého filtru zadejte **D8100** pro vyhledání existujícího uvolněného produktu.

    ![Filtrování uvolněného produktu D8100 na stránce Podrobnosti uvolněného produktu](./media/subcontract02_filtering-released-products.png)

3. V podokně akcí na kartě **Analýza** zvolte **Postup** k otevření stránky **Postup**.

    Stránka **Postup** zobrazuje osm verzí postupu pro uvolněný produkt D8100. Osm verzí postupu je rozděleno mezi čtyři postupy na pracovišti 1 a pracovišti 5. Postup 000400 se používá pro výpočet nákladů, postup 00041 se používá, když je lakování interní operací a postup 00042 se používá tehdy, když je lakování externí operací.

    ![Osm verzí postupu na stránce Postup](./media/subcontract03_route-page.png)

4. V horním podokně v mřížce **Verze** zvolte verzi postupu **00042** pro pracoviště **5**.
5. V dolním podokně na **Přehled** zvolte operaci **20** (**Cbnt CtSc**) v mřížce.

    ![Je zvolena operace 20 pro verzi postupu 00042 pro pracoviště 5](./media/subcontract04_route-version-operation.png)

6. Zvolte kartu **Obecné**.

    Všimněte si, že pole **Typ postupu** je nastaveno na **Dodavatel**. Tato hodnota označuje, že operace 20 (Cbnt CtSc) je subdodavatelskou operací.

    ![Pole typ postupu nastavené na Dodavatel na kartě Obecné](./media/subcontract05_general-tab.png)

7. Zvolte kartu**Požadavky na zdroj**.

    Možnosti budou použity pro vyhledání použitelného zdroje během plánování výroby. U operace 20 (Cbnt CtSc) 20 si všimněte, že je nutný zdroj s dvěma možnostmi **Lakování** a **Lakované skříňky**.

    ![Možnosti Lakování a Lakované skříňky na kartě požadavků na zdroj](./media/subcontract06_resource-requirements-tab.png)

8. Zvolte **Použitelné prostředky** a otevřete dialogové okno **Použitelné prostředky**.

    Byly nalezeny tři zdroje, které splňují požadavky na zdroje pro operaci. Všimněte si, že zdroje 8851 a 8852 jsou typem **Dodavatel**.

    ![Tři vhodné zdroje v dialogovém okně Použitelné prostředky](./media/subcontract07_applicable-resources-dialog.png)

9. Vyberte **OK**, zavřete dialogové okno **Použitelné prostředky** a vraťte se na stránku **Postup**.
10. Zavřete stránku **Postup** a vraťte se na stránku **Podrobnosti uvolněného produktu**.

    ![Stránka podrobností o uvolněném produktu](./media/subcontract08_released-product-details-page.png)

11. V podokně akcí na kartě **Analýza** zvolte **Verze kusovníku** k otevření stránky **Verze kusovníku**.

    Stránka **Verze kusovníku** zobrazuje čtyři verze kusovníku pro uvolněný produkt D8100. Kusovník 000040 se používá pro výpočet nákladů a plánování, kusovník 000041 se používá, pokud je operace lakování prováděna interně a kusovníky 000042 a 000043 se používají v případě, že je operace lakování .subdodavatelskou aktivitou.

    Všimněte si, že položka S8050 je produktem typu položky **Služba**. Tato položka reprezentuje práci subdodavatele.

    ![Čtyři verze kusovníku na stránce verzí kusovníku](./media/subcontract09_bom-versions-page.png)

12. Na pevné záložce **Řádky kusovníku** zvolte **Upravit** a otevřete dialogové okno **Upravit řádek kusovníku**.

    Po vytvoření a ocenění výrobní zakázky pro uvolněný produkt D8100 bude automaticky vygenerována nákupní objednávka pro položku S8050. Tato nákupní objednávka bude propojena na výrobní zakázku. Aby mohly být automaticky vygenerovány nákupní objednávky, je třeba nastavit **Typ řádku** na **Dodavatel** a musí být vybrán účet dodavatele pro subdodavatele. V tomto případě je účet dodavatele US-801.

    Všimněte si, že řádek kusovníku je připojen k operaci lakování prostřednictvím čísla operace (v tomto případě 20).

    ![Úprava dialogové okna řádku kusovníku](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Vytvoření hesla pro pracovníky skladu

Musíte definovat heslo pro pracovníky skladu, kteří používají ruční zařízení.

1. Vyberte **Řízení skladu \> Nastavení \> Pracovník** a otevřete stránku **Uživatelé práce**.
2. Na pevné záložce **Uživatelé** vyberte řádek pro uživatele **51**.

    ![Stránka uživatelů práce](./media/subcontract11_work-users-page.png)

3. Zvolte **Resetovat heslo**.
4. V polích **Heslo** a **Potvrdit heslo** zadejte **1**.
5. Zvolte **Nastavit heslo**.

## <a name="step-by-step-walkthrough"></a>Ukázka krok za krokem

**Scénář a pozadí**

Je vytvořena výrobní zakázka na 10 kusů pro produkt D8100, „Nalakovaná skříňka.“ Lakování skříněk je subdodavatelská operace, která se provádí u dodavatele USA 801, Perfect Coating Solutions. Výrobní zakázka se skládá ze tří operací. V první operaci je skříňka předběžně sestavena v rámci interní operace. Materiál pro předběžné sestavení je uvolněn k výdeji ve skladu surovin. Po dokončení předběžného sestavení je skříňka odeslána do společnosti Perfect Coating Solutions spolu s dvěma materiály, které jsou zapotřebí pro operaci lakování. Když je nalakovaná skříňka vrácena zpět od dodavatele, projde operací konečného sestavní, než je označena jako dokončená.

1. Vyberte **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete stránku **Všechny výrobní zakázky**.
2. V podokně akcí zvolte **Nová výrobní zakázka** a otevřete dialogové okno **Vytvořit výrobní zakázku**.

    ![Vytvoření dialogového okna výrobní zakázky](./media/subcontract12_create-production-order-dialog.png)

3. V poli **Číslo položky** zvolte **D8100**.
4. Pole dimenzí zásob se zobrazí po výběru čísla položky. V poli **Barva** vyberte **Chromovaná**.

    Objeví se okno s dotazem, zda se mají vložit aktivní verze kusovníku a postupu.

    ![Okno se zprávou](./media/subcontract13_message-box.png)

5. Vyberte **Ano**. 

    V dialogovém okně **Vytvořit výrobní zakázku** jsou automaticky zvoleny aktivní verze kusovníku a postupu pro produkt D8100 v polích **Číslo kusovníku** a **Číslo postupu**. V tomto případě jsou vybrány kusovník **000040** a postup **000040**.
    
    > [!NOTE]
    > Pro kusovník a postup se používá verze 000040 pro výpočet nákladů a plánování.

6. V poli **Pracoviště** zvolte **5**.
7. V poli **Sklad** zvolte **51**.
8. V polích **Číslo kusovníku** a **Číslo postupu** změňte hodnotu, která byla automaticky vybrána, na **000042**.

    > [!NOTE]
    > Pro kusovník a postup se použije verze 000042 pro postoupení subdodávky lakování skříňky dodavateli US-801.

    ![Hodnoty nastavené v dialogovém okně Vytvořit výrobní zakázku](./media/subcontract14_create-production-order-dialog-set.png)

9. Vyberte **Vytvořit** pro vytvoření výrobní zakázky a přejdete zpět na stránku **Všechny výrobní zakázky**.

    ![Nová výrobní zakázka na stránce Všechny výrobní zakázky](./media/subcontract15_new-production-order.png)

10. V podokně akcí na kartě **Výrobní zakázka** zvolte **Odhad** pro otevření dialogového okna **Odhad**.

    ![Dialogové okno Odhad](./media/subcontract16_estimate-dialog.png)

11. Vyberte **OK** pro potvrzení odhadu a přejdete zpět na stránku **Všechny výrobní zakázky**.

    > [!NOTE]
    > Když je výrobní zakázky oceněna, vygeneruje se nákupní objednávka pro servisní položku S8050 pro dodavatele US-801.

12. V podokně akcí na kartě **Výrobní zakázka** zvolte **Kusovník** pro otevření stránky **Kusovník** , kde můžete zobrazit řádky kusovníku pro výrobní zakázku.

    U servisní položky S8050 si všimněte, že existuje odkaz na nákupní objednávku, která byla vygenerována při ocenění výrobní zakázky.

    ![Řádky kusovníku výrobní zakázky na stránce kusovníku](./media/subcontract17_production-order-bom-lines.png)

13. Zavřete stránku **Kusovník** a vraťte se na stránku **Všechny výrobní zakázky**.
14. V podokně akcí na kartě **Plán** zvolte **Plánovat úlohy** pro otevření dialogového okna **Plánování úlohy**.
15. Určete následující hodnoty:

    - V poli **Způsob plánování** vyberte **Vpřed od zítřka**.
    - Nastavte možnost **Omezená kapacita** na **Ano**.

    ![Dialogové okno plánování úlohy](./media/subcontract18_job-scheduling-dialog.png)

16. Vyberte **OK**, zavřete dialogové okno **Plánování úlohy** a vraťte se na stránku **Všechny výrobní zakázky**.
17. V podokně akcí na kartě **Plán** zvolte **Ganttův diagram** a otevřete stránku **Ganttův diagram – Zobrazení zdrojů**.

    Ganttův diagram obsahuje grafické znázornění plánování výrobních úloh na prostředcích. Všimněte si, že externí operace nátěru se skládá ze tří úloh: úloha zpracování, úloha přepravy a úloha času čekání.

    ![Ganttův diagram na stránce Ganttův diagram - Zobrazení zdrojů](./media/subcontract19_gantt-chart.png)

18. Zavřete stránku **Ganttův diagram - Zobrazení zdrojů** a vraťte se na stránku **Všechny výrobní zakázky**.
19. V podokně akcí na kartě **Výrobní zakázka** zvolte **Uvolnění** pro otevření dialogového okna **Uvolnění**.

    ![Dialogové okno uvolnění](./media/subcontract20_release-dialog.png)

20. Zvolte **OK** a zavřete dialogové okno **Uvolnění**.
21. Vyberte **Řízení výroby \> Pravidelné úlohy \> Uvolnění do skladu \> Automaticky uvolnit řádky kusovníku a receptury** a otevřete dialogové okno **Automaticky uvolnit řádky kusovníku a receptury**.

    ![Dialogové okno Automaticky uvolnit řádky kusovníku a receptury](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Vyberte **OK** a spusťte úlohu Automaticky uvolnit řádky kusovníku a receptury.

    Tato úloha uvolní práci výdeje pro suroviny do skladu.

23. Vyberte **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete stránku **Všechny výrobní zakázky**.
24. Použijte pole rychlého filtru pro volbu výrobní zakázky, na které jste pracovali.
25. V podokně akcí na kartě **Sklad** zvolte **Podrobnosti práce** k otevření stránky **Práce**.

    Všimněte si, že stránka zobrazuje dvě sady práce pro výdej suroviny. První práce je pro materiály M8100 a M8101. Tyto materiály jsou spotřebovány operací 10. Druhá práce je pro materiály M8202 a M8250. Tyto materiály spotřebovává operace 20, což je operace subdodavatele.

    ![Dvě sady práce pro výdej suroviny na stránce Práce](./media/subcontract22_work-page.png)

26. Spusťte aplikaci skladu ke zpracování práce skladu pro operaci 10.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Vyberte **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete stránku **Všechny výrobní zakázky**.
28. Použijte pole rychlého filtru pro volbu výrobní zakázky, na které jste pracovali.
29. V podokně akcí na kartě **Výrobní zakázka** zvolte **Spustit** pro otevření dialogového okna **Spustit**.
30. Na kartě **Obecné** zadejte následující hodnoty:

    - V poli **Od operace č.** zvolte **10**.
    - V poli **Do operace č.** zvolte **10**.

    ![Hodnoty nastavené na kartě Obecné](./media/subcontract23_start-dialog.png)

31. Vyberte **OK**, zavřete dialogové okno **Spustit** a vraťte se na stránku **Všechny výrobní zakázky**.

    Všimněte si, že stav výrobní zakázky je nyní **Spuštěno**. Materiály pro operaci 10 se spotřebují automatickým zaúčtováním deníku výdejek. Spotřeba času pro operaci 10 je zaúčtována automatických zaúčtováním deníku karet postupů.

32. Spusťte aplikaci skladu ke zpracování práce skladu pro operaci 20.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. V podokně akcí na kartě **Výrobní zakázka** zvolte **Spustit** pro otevření dialogového okna **Spustit**.
34. Na kartě **Obecné** zadejte následující hodnoty:

    - V poli **Od operace č.** zvolte **20**.
    - V poli **Do operace č.** zvolte **20**.
    - Do pole **Množství** zadejte **10**.
    - Nastavte možnost **Zaúčtovat výdejku** na **Ne**.

    ![Hodnoty nastavené na kartě Obecné](./media/subcontract24_general-tab.png)

35. Vyberte **OK**, zavřete dialogové okno **Spustit** a vraťte se na stránku **Všechny výrobní zakázky**.

    Je vytvořena výdejka pro materiály, které jsou použity pro operaci lakování, a pro servisní položku. Servisní položka reprezentuje náklady za subdodavatelskou operaci.

36. V podokně akcí na kartě **Zobrazení** zvolte **Výdejka** a otevřete stránku **Výdejka**.
37. Vyberte výdejku, která není zaúčtována, a poté vyberte číslo deníku pro zobrazení řádků deníku.

    ![Řádky deníku na stránce Výdejka](./media/subcontract25_picking-list.png)

38. V podokně akcí zvolte **Tisk** \> **Sestava výdejky** a otevřete dialogové okno **Sestava výdejky**.
39. Nastavte možnost **Použít rozvržení poznámky k dodání** na **Ano**.

    ![Dialogové okno sestavy výdejky](./media/subcontract26_picking-list-report-dialog.png)

40. Zvolte **OK** pro vygenerování sestavy **Výdejka**.

    V takovém případě se vytiskne poznámka k dodání od dodavatele z deníku výrobních výdejek. Poznámka k dodání určuje materiály expedované dodavateli, který provede operaci lakování.

    ![Sestava výdejky](./media/subcontract27_picking-list-report.png)

41. Zavřete sestavu **Výdejka** a vraťte se na stránku **Výdejka**.
42. V podokně akcí zvolte **Zaúčtovat** a otevřete dialogové okno **Zaúčtovat deník**.

    ![Dialogové okno Zaúčtování deník](./media/subcontract28_post-journal-dialog.png)

43. Zvolte **OK** a zavřete dialogové okno **Zaúčtování deník**.
44. Otevřené nákupní objednávku.

    ![Stránka nákupní objednávky](./media/subcontract29_purchase-order-page.png)

45. V podokně akcí na kartě **Nákup** zvolte **Potvrdit**.
46. Zvolte **Zaúčtovat** a otevřete dialogové okno **Zaúčtování deník**.
47. Vyberte **OK**, zavřete dialogové okno **Zaúčtovat deník** a vraťte se na stránku **Nákupní objednávka**.
48. Změňte jednotkovou cenu z **33** na **40**.

    ![Změněná jednotková cena na stránce Nákupní objednávka](./media/subcontract30_unit-price.png)

49. Potvrďte znovu nákupní objednávku.
50. Příjemka produktu.

    ![Dialogové okno Zaúčtování příjemky produktu](./media/subcontract31_posting-product-receipt-dialog.png)

51. Nákupní faktura.
52. Aktualizujte stav párování.

    ![Stránka faktury dodavatele](./media/subcontract32_vendor-invoice-page.png)

53. Hlášení jako dokončené.

    ![Dialogové okno Hlášení jako dokončené](./media/subcontract33_report-as-finished-dialog.png)

54. Ukončit.

    ![Dialogové okno Ukončit](./media/subcontract34_end-dialog.png)

55. Porovnání nákladů.

    ![Graf porovnání nákladů](./media/subcontract35_cost-comparison-charts.png)

Chybí nastavení v datech.
