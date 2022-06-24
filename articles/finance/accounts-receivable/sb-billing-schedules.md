---
title: Vytvoření plánů fakturace
description: Tento článek vysvětluje, jak vytvořit, odstranit a upravit plány fakturace.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903385"
---
# <a name="create-billing-schedules"></a>Vytvoření plánů fakturace

[!include [banner](../includes/banner.md)]

Na stránce **Plán fakturace** můžete vytvářet, odstraňovat nebo upravovat plány fakturace. Můžete si také prohlédnout seznam plánů fakturace. Když vytvoříte plán fakturace, výchozí hodnoty pro něj jsou určeny fakturační skupinou, která je k němu přidružena. Další informace jsou nastaveny na stránce **Parametry opakované fakturace smlouvy**.

## <a name="create-a-billing-schedule"></a>Vytvoření plánu fakturace

Při vytváření plánu fakturace postupujte takto:

1. Na stránce **Plány fakturace** vyberte položku **Nový**.
2. V dialogu **Vytvořit plán fakturace** vyberte v poli **Skupina plánů fakturace** skupinu plánů fakturace.
3. V poli **Účet zákazníka** vyberte účet zákazníka.
4. V poli **Počáteční datum** vyberte počáteční datum a poté v poli **Počet období** zadejte počet období. Pole **Datum ukončení** se aktualizuje na základě počtu období, které zadáte. Pokud aktualizujete pole **Koncové datum fakturace**, pole **Počet období** se aktualizuje na **0** (nula).
5. Vyberte **OK**.
6. Na stránce **Plán fakturace** na kartě **Obecné** zadejte v poli **Popis** popis plánu fakturace.
7. V poli **Šablona milníku** vyberte šablonu milníku pro **Vyúčtování po milnících**.

Pole **Fakturační účet** a **Kód měny** jsou aktualizovány informacemi od zákazníka.

Pole **Četnost fakturace** a **Interval fakturace** jsou automaticky nastavena na základě vybrané skupiny plánů fakturace.

8. Chcete-li vytvořit samostatné faktury, nastavte možnost **Faktura zvlášť** na **Ano**.
9. Chcete-li automaticky obnovit plán fakturace po posledním zúčtovacím období, nastavte možnost **Obnovit automaticky** na **Ano** a poté nastavte pole **Řádky, které se mají přidat při obnovení**.

Pole **Parametry** jsou automaticky nastavena na základě hodnot na stránce **Parametry opakované fakturace smlouvy**.

10. Chcete-li částku plánu fakturace poměrně rozdělit, nastavte možnost **Poměrně rozdělit částečná období** na **Ano**.
11. Chcete-li vyrovnat řádky podrobností plánu fakturace s koncem měsíce, nastavte možnost **Vyrovnat podle měsíce** na **Ano**.
12. V poli **Počáteční datum smlouvy** a **Koncové datum smlouvy** zadejte počáteční a koncové datum smlouvy. Tato kalendářní data jsou pouze informativní.

Pole **Způsob platby** zobrazuje informace o platbě od zákazníka. Když je řádková položka pozastavena nebo ukončena, platební údaje nelze změnit.

> [!NOTE]
> Když konsolidujete faktury podle položek, hodnota polí **Platební podmínky**, **Metoda** a **Plán fakturace** se musejí shodovat. V opačném případě nelze faktury konsolidovat.

13. Na kartě **Adresa** můžete zkontrolovat a aktualizovat pole **Doručovací adresa** a **Adresa příjemce faktury**.
14. Na kartě **Kontaktní informace** můžete přiřadit účet koncového uživatele k plánu fakturace.
15. V polích **Kontaktní informace** můžete zadat kontakt, e-mailovou adresu a internetovou adresu.
16. Chcete-li sledovat informace o provizi partnera, nastavte pole **Partnerský účet** a **Sazba provize partnera**. Tato pole jsou pouze informativní.
17. Na kartě **Celkem** můžete zobrazit různé součty, které byly vypočteny pro plán fakturace.
18. Na kartě **Blokování** můžete zobrazit informace auditu o tom, kdy byl plán fakturace pozastaven, když bylo pozastavení odstraněno.
19. Na kartě **Ukončení** můžete zobrazit historii ukončení, která byla použita nebo odstraněna z plánu fakturace.
20. Zvolte možnost **Uložit**.
21. Na záložce **Řádky plánu fakturace** vyberte **Přidat řádek**.
22. V poli **Číslo položky** vyberte číslo položky. Pokud je přidaná položka nadřazenou položkou v rozdělení příjmů, řádky se automaticky aktualizují podřízenými položkami. V rozdělení příjmů můžete upravit pouze nadřazenou položku. Všechny podřízené položky jsou poté odpovídajícím způsobem aktualizovány.
23. V poli **Typ položky** vyberte typ položky.
24. Aktualizujte počáteční a koncové datum.
25. Před vytvořením faktur můžete změnit četnost fakturace aktualizací pole **Četnost fakturace**. Po vytvoření první faktury pro plán fakturace nelze četnost fakturace změnit.
26. V poli **Jednotka** vyberte měrnou jednotku pro položku.
27. V poli **Způsob stanovení ceny** vyberte metodu stanovení ceny pro položku.

Pole **Jednotková cena** je automaticky nastaveno ze skladu. Můžete jej však aktualizovat, pokud změníte způsob stanovení ceny na **Paušální**.

## <a name="remove-a-line-item"></a>Odebrání řádkové položky

Chcete-li odebrat položku z plánu fakturace, postupujte takto.

1. Na stránce **Plán fakturace** vyberte v poli **Číslo plánu** číslo plánu fakturace, který chcete upravit.
2. Na záložce **Řádky plánu fakturace** vyberte řádek, který chcete odstranit, a poté vyberte **Odstranit**.
3. Zvolte možnost **Uložit**.

Zbytek tohoto článku popisuje akce a podrobnosti, které jsou pro řádky k dispozici na záložce **Řádky plánu fakturace**.

## <a name="billing-schedule-line-actions"></a>Akce řádků plánu fakturace

Tlačítka na záložce **Řádky plánu fakturace** umožňují aplikovat akce na jednotlivé řádky.

| Tlačítko | Popis |
|--------|-------------|
| Přidat řádek | Přidání řádku do plánu fakturace. |
| Přidat ze seznamu položek | Přidání více položek do plánu fakturace jejich výběrem v seznamu. |
| Odebrat | <p>Odebrání vybraného řádku z plánu fakturace.</p><p>U položek, které jsou součástí rozdělení příjmů, můžete odebrat pouze nadřazenou položku. Všechny přidružené podřízené položky jsou poté automaticky odstraněny.</p> |
| Zobrazit podrobnosti fakturace | Zobrazení podrobností fakturace. |
| Ukončit | <p>Ukončení vybraných řádků. Toto tlačítko je dostupné pouze v případě, že vybrané řádky mají stav **Aktivní**.</p><p>U položek, které jsou součástí rozdělení příjmů, můžete ukončit pouze nadřazenou položku.</p> |
| Odstranit ukončení | <p>Odebrání ukončení z vybraných řádků. Toto tlačítko je dostupné pouze v případě, že vybrané řádky mají stav **Ukončeno**.</p><p>U položek, které jsou součástí rozdělení příjmů, můžete odebrat ukončení pouze z nadřazené položky.</p> |
| Blokovat | <p>Vyberte podrobnosti pro pozastavení vybraného řádku.</p><p>U položek, které jsou součástí rozdělení příjmů, můžete pozastavit pouze nadřazenou položku.</p> |
| Odstranit blokování | <p>Odebrání pozastavení z vybraného řádku.</p><p>U položek, které jsou součástí rozdělení příjmů, můžete odebrat pozastavení pouze z nadřazené položky.</p> |
| Eskalace a sleva | Toto tlačítko není dostupné u položek, které jsou součástí rozdělení příjmů, kromě nadřazených položek, kde rozdělení příjmů používá metodu přidělení **Nulové množství**. |
| Časově rozlišené položky | <p>Zadejte možnosti odložení pro vybraný řádek.</p><p>Toto tlačítko není k dispozici pro nadřazené položky v rozdělení příjmů.</p> |
| Přidělení milníku | <p>Zkontrolujte a aktualizujte informace o přidělení milníku pro vybraný řádek.</p><p>Toto tlačítko je dostupné pouze v případě, že je řádková položka plánu fakturace milníkem.</p> |
| Podpora a obnovení | <p>Zkontrolujte a aktualizujte informace o podpoře a obnovení pro vybraný řádek.</p><p>Toto tlačítko je dostupné pouze v případě, že je řádková položka plánu podporou nebo obnovením.</p> |
| Zobrazit dimenze | Zobrazte nebo skryjte sloupce dimenzí, které se zobrazují v mřížce **Řádky plánu fakturace**. |
| Vypočítat cenu za jednotku | <p>Vypočítejte jednotkovou cenu položky, aby zákazník mohl uhradit smluvní částku ve splátkách (například denně, měsíčně, čtvrtletně, pololetně nebo ročně). Můžete si vybrat smluvní cenu a cenovou frekvenci.</p><p>Můžete si prohlédnout auditní záznam změn: starou smluvní cenu a frekvenci, novou smluvní cenu a frekvenci, uživatele, který provedl změnu, a datum a čas změny.</p> |
| Datum vyrovnání | <p>Zadejte datum vyrovnání pro položky obnovení.</p><p>Pokud vyberete skupinu položek v poli **Skupina položek**, všechny položky používají datum vyrovnání první položky ve skupině položek v plánu fakturace. Pokud je pole **Skupina položek** prázdné, můžete zadat datum vyrovnání, které se má použít pro všechny položky.</p><p>Toto tlačítko je dostupné pouze v případě, že pole **Četnost fakturace** je nastaveno na **Roční**.</p> |
| Nevyfakturované výnosy | <p>Nastavte položku tak, aby používala funkci nevyfakturovaných příjmů. Poté můžete zadat nevyfakturované výnosy a účty nevyúčtovaných slev pro položku.</p><p>Toto tlačítko je dostupné pouze pro položky, kde je **Typ položky** nastaven na **Standardní**. Není k dispozici pro existující plány fakturace ani pro řádky plánu fakturace, kde již byla vytvořena faktura.</p> |
| Přidat podřízenou položku rozdělení výnosů | <p>Vyberte podřízenou položku, kterou chcete přidat do prodejní objednávky.</p><p>Toto tlačítko je k dispozici pouze pro nadřazené položky v rozdělení příjmů.</p> |
| Rozšířené možnosti tvorby cen | Upravte možnosti cen pro položku. |

## <a name="billing-schedule-line-details"></a>Podrobnosti řádků plánu fakturace

Když vyberete řádek na záložce **Řádky plánu fakturace**, můžete zobrazit konkrétní podrobnosti pro tento řádek. Tyto podrobnosti jsou rozděleny mezi různé karty.

### <a name="general-tab"></a>Karta Obecné

Na kartě **Obecné** jsou k dispozici následující informace.

| Pole nebo sekce | Popis |
|------------------|-------------|
| Použití | <p>Tato sekce poskytuje informace o položkách využití. Obsahuje následující pole:</p><ul><li>**Identifikátor použití** – Identifikátor měřiče nebo položky použití.</li><li>**Možnost čtení** – Možnost čtení použití: **Čtení** nebo **Spotřeba**.</li><li>**Odhadovaná spotřeba** – Zadejte odhadovanou spotřebu pro položku použití, která má období, kdy faktura nebyla vytvořena. Na stránce **Detail fakturace** můžete zkontrolovat řádky fakturačních podrobností pro odhadovanou spotřebu.</li></ul> |
| Externí odkazy\* | Tato sekce obsahuje pole **Externí** a **Číslo řádku**, kde můžete zadat externí referenční informace. |
| Milník | <p>Tato sekce poskytuje informace o položkách milníků. Obsahuje pole **Předpokládané datum dokončení**, které zobrazuje datum dokončení položky.</li></ul> |
| Text | Komentář k řádku. Text je přeložen do výchozího jazyka zákazníka nebo právnické osoby. |
| Sk. položek | Skupina položek pro řádkovou položku. |
| Datum vyrovnání | Datum vyrovnání pro plán fakturace. |

\* Když konsolidujete faktury podle položek na stránce **Vygenerovat fakturu**, pole **Externí reference** se musejí shodovat. Pokud se byť jen jeden znak liší, položky nebudou na faktuře sloučeny. Žádné ověřovací kontroly se neprovádějí v žádném poli sekce **Externí reference** a hodnota v poli **Číslo řádku** musí být kladné celé číslo.

### <a name="address-tab"></a>Karta Adresa

Na kartě **Adresa** jsou k dispozici následující informace.

| Pole | Popis |
|-------|-------------|
| Adresa dodání | <p>Vyberte dodací adresu pro řádkovou položku. Výchozí dodací adresa je primární dodací adresa ze záložky **Adresa**.</p><p>Když změníte adresu, můžete vybrat následující možnosti adresy:</p><ul><li>**Adresy** – Vyberte adresu pro aktuálního zákazníka.</li><li>**Používá se** – Vyberte adresu, která se aktuálně pro aktuálního zákazníka používá.</li><li>**Jiná adresa** – Vyberte adresu pro libovolný záznam zákazníka.</li></ul><p>U položek, které používají rozdělení příjmů, lze upravit pouze adresu nadřazené položky. Adresa podřízených položek se shoduje s adresou nadřazené položky a nelze ji samostatně upravovat.</p> |
| Adresa příjemce faktury | <p>Vyberte adresu příjemce faktury pro řádkovou položku. Výchozí dodací adresa je primární dodací adresa ze záložky **Adresa**. Adresu můžete libovolně změnit na základě účelu dostupných adres:</p><ul><li>Pokud žádná z adres nemá účel **Faktura**, výchozí fakturační adresa je primární adresou zákazníka bez ohledu na účel.</li><li>Pokud má jedna nebo více adres účel **Faktura**, výchozí fakturační adresou je adresa, která byla zadána naposledy.</li><li>Pokud má jedna nebo více adres účel **Faktura** a jedna z fakturačních adres je nastavena jako primární, výchozí fakturační adresou je adresa, která má účel **Faktura** a je nastavena jako primární.</li><li>U položek, které používají rozdělení příjmů, lze upravit pouze adresu nadřazené položky. Adresa podřízených položek se shoduje s adresou nadřazené položky a nelze ji samostatně upravovat.</li></ul> |

### <a name="product-tab"></a>Karta Produkt

Na kartě **Produkt** jsou k dispozici následující informace.

| Pole nebo sekce | Popis |
|------------------|-------------|
| Dimenze úložiště | <p>Tato část zobrazuje informace o úložišti položky. Obsahuje pole **Sériové číslo**, které zobrazuje sériové číslo položky.</p><p>Sériové číslo se zkopíruje z počáteční prodejní objednávky během procesu podpory a obnovy. U položek, které používají rozdělení výnosů, se sériové číslo nadřazené položky zkopíruje do všech podřízených položek. Sériové číslo se zkopíruje, když je možnost **Zkopírovat sériové číslo** nastavena na **Ano** ve stránce **Parametry opakované fakturace smlouvy**.</li></ul> |
| Dimenze produktu | Podrobnosti o produktu pro položku a hodnoty se automaticky aktualizují na základě hodnoty **Číslo varianty**, která je vybrána pro řádek plánu fakturace. |

### <a name="account-tab"></a>Karta Účet

Na kartě **Účet** jsou k dispozici následující informace.

| Pole | Popis |
|-------|-------------|
| Hlavní účet | Hlavní účet, který je vytvořen na prodejním řádku. Výchozí hodnota je z prodejní objednávky. Toto pole může být prázdné. |
| Finanční dimenze položky | <p>Výchozí hodnoty finanční dimenze na základě záznamu zákazníka a položky.</p><p>U položek, které používají rozdělení výnosů, používají podřízené položky hodnoty finančních dimenzí zákazníků a záznamů položek, jak bylo popsáno výše. Pokud musíte aktualizovat hodnoty finanční dimenze podřízených položek, můžete importovat datovou entitu.</p> |

### <a name="renewals-tab"></a>Karta Obnovení

Na kartě **Obnovení** jsou k dispozici následující informace.

| Pole | Popis |
|-------|-------------|
| Automaticky obnovit | <p>Hodnota, která udává, zda se řádek plánu fakturace automaticky obnoví pro další fakturační období:</p><ul><li>**Ano** – Řádek plánu fakturace automaticky obnoví pro další fakturační období při vytvoření faktury.</li><li>**Ne** – Řádek plánu fakturace se automaticky neobnovuje. Plán fakturace musíte obnovit ručně.</li></ul> |
| Řádky, které se mají přidat na obnovení | Počet řádků, které se mají přidat do obnovení plánu fakturace. |

Na kartě **Obnovení** jsou dále k dispozici následující tlačítka.

| Tlačítko | Popis |
|--------|-------------|
| Audit zápisu do deníku nevyfakturovaných výnosů | Zobrazí všechny změny u položek, které používají funkci nevyfakturovaných příjmů. |
| Přidat termín obnovení | Přidejte termín obnovení pro položku. Počáteční datum nového období obnovení je datum následující po datu ukončení předchozího období. Pole **Datum ukončení obnovení**, **Datum odloženého začátku**, **Datum ukončení odkladu**, **Množství položky** a **Jednotková cena** lze aktualizovat. |
| Změnit termín obnovení | <p>Upravte termín obnovení. Pro počáteční období můžete změnit počáteční a koncové datum odložení před vytvořením počátečního zápisu do deníku. U dalších období nelze datum zahájení změnit. Je to vždy datum následující po skončení předchozího období.</p><p>Pokud po období, které upravujete, existuje období obnovení, data období nelze změnit. V tomto případě lze aktualizovat pouze pole **Množství** a **Jednotková cena** pro položku obnovení.</p><p>Například existují tři období. <ul><li>První období nelze změnit, protože již začalo.</li><li>U druhého období lze změnit pouze množství a jednotkovou cenu.</li><li>U třetího období lze změnit všechny hodnoty kromě data zahájení. Kromě toho možnost **Plán ze šablony** umožňuje vytvořit plán odkladu, který je založen na šabloně pro položku nevyfakturovaných výnosů. Když je tato možnost nastavena na **Ano**, vyberte šablonu odložení v poli **Šablona** a podle potřeby změňte datum zahájení a ukončení odkladu. Následné období obnovení používají stejnou šablonu odkladu. Šablonu odkladu však lze změnit.</p></li></ul> |

### <a name="termination-tab"></a>Karta Ukončení

Na kartě **Ukončení** jsou k dispozici následující informace.

| Pole | Popis |
|-------|-------------|
| Datum výpovědi | Datum ukončení řádku plánu fakturace. Výchozí hodnota pochází z pole **Datum ukončení** v záhlaví. Hodnotu v tomto poli můžete podle potřeby měnit. |
| Typ ukončení | Typ ukončení. Výchozí hodnota pochází z pole **Typ ukončení** v záhlaví. |

### <a name="hold-tab"></a>Karta Blokování

Pokud se použije odložení výnosů a nákladů, karta **Blokování** karta zobrazuje datum odkladu.

### <a name="escalation-and-discount-tab"></a>Karta Eskalace a slevy

Na kartě **Eskalace a slevy** jsou k dispozici následující informace.

| Pole | Popis |
|-------|-------------|
| Eskalace | <p>Vyberte, zda jsou pro řádek plánu fakturace povoleny eskalace. Jakýkoli řádek eskalace ze záhlaví se použije při vytvoření řádku plánu fakturace.</p><ul><li>**Ano** – Na řádek lze aplikovat eskalace. Když je vybrána tato možnost, můžete nastavit eskalace pro řádky plánu fakturace na stránce **Eskalace a sleva**.</li><li>**Ne** – Na řádek nelze aplikovat eskalace.</li></ul><p>Výchozí nastavení je založeno na vybrané **Skupině plánů fakturace**.</p> |

### <a name="price-changes-tab"></a>Karta Změny cen

U řádků, které mají změněnu **Standardní** cenu na **Paušální**, obsahuje mřížka na kartě **Změny cen** následující sloupce:

- Změnit datum
- Změněno uživatelem
- Standardní cena
- Paušální cena
- Aktualizace ceny
