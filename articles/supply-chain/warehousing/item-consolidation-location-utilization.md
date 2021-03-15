---
title: Konsolidace zboží - Využití skladového místa
description: Toto téma poskytuje informace o funkcích, které usnadňují vedoucím skladu prohlížet a filtrovat objemové využití umístění v celém skladu. Manažeři mohou vybírat místa a vytvářet pohyby inventáře přímo ze stránky Konsolidace položek, aby konsolidovali položky, a proto lépe využívali skladové prostory.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004645"
---
# <a name="item-consolidation---location-utilization"></a>Konsolidace zboží - Využití skladového místa

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o funkcích, které usnadňují vedoucím skladu prohlížet a filtrovat objemové využití umístění v celém skladu. Manažeři mohou vybírat místa a vytvářet pohyby inventáře přímo ze stránky **Konsolidace položek**, aby konsolidovali položky, a proto lépe využívali skladové prostory.

## <a name="turn-on-the-features"></a>Zapnutí funkcí

Než budete moci používat funkce popsané v tomto tématu, musíte je v systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav těchto funkcí a dle potřeby je zapnout. Zapněte obě následující funkce v pořadí, v jakém jsou uvedeny v seznamu. (Obě funkce jsou pro modul **Správa skladu**.)

1. Stav umístění ve skladu
2. Využití skladového místa pro konsolidaci zboží

## <a name="warehouse-location-status"></a>Stav umístění ve skladu

Funkce *Stav umístění skladu* přidá čtyři nová pole na stránku **Místa** pro sledování dalších informace o aktuálním stavu místa:

- **Číslo položky** – položka, která je aktuálně na skladovém místě. Pokud skladové místo obsahuje více položek, bude toto pole prázdné.
- **Datum a čas poslední aktivity** – časové razítko poslední skladové transakce provedené v daném skladovém místě.
- **Datum pro sledování stárnutí** – datum, kdy byly zásoby ve skladovém místě přivezeny do skladu. Toto datuj se vypočítává na základě data stárnutí registrační značky. Přestože je toto datum přesné pro skladová místa, pro něž se využívá měření podle registračních značek, nemusí být přesné v případě skladových míst, jež takto sledována nejsou.
- **Stav skladového místa** – stav skladového místa. K dispozici jsou čtyři hodnoty:

    - **Neurčeno** – profil skladového místa stav nesleduje. Aktuální stav proto není známý.
    - **Prázdné** – ve skladovém místě nejsou v současné době žádné zásoby.
    - **Výdej** – ve skladovém místě byly od doby, kdy bylo naposledy prázdné, provedeny odchozí transakce.
    - **Skladování** – od doby, kdy bylo skladové místo naposledy prázdné, byly prováděny pouze příchozí transakce.

Tato pole umožňují manažerům skladu mít lepší přehled o stavu skladových míst ve skladu. Umožňují také pokročilejší vykazování a filtrování.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Nastavení konsolidace zboží a využití skladového místa

Tato část popisuje, jak připravit systém k použití konsolidace položek a využití umístění. Postupy používají ukázkové hodnoty ze standardních demonstračních dat. Pokud se chystáte projít cvičná scénář, který je uveden dále v tomto tématu, vyberte právnickou osobu **USMF** (která obsahuje standardní demo data) a vytvořte každý záznam popsaný v této části. Pokud neplánujete pracovat s ukázkovým scénářem, mohou být hodnoty, které jsou zde uvedeny, považovány za příklady typů nastavení, které musíte pro použití funkcí dokončit.

### <a name="released-product"></a>Uvolněný produkt

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. V poli **Číslo položky** vyberte *M9201* a otevřete stránku podrobností.
1. V podokně Akce na kartě **Správa zásob** ve skupině **Sklad** vyberte **Fyzické rozměry**.
1. Na stránce **Fyzické rozměry** v podokně Akce vyberte **Nový**.

    Do mřížky je přidán nový řádek. Pole **Číslo položky** je přednastaveno.

1. V poli **Jednotka** pak vyberte možnost *ea*. Zbývající pole na řádku se nastaví automaticky.
1. Zvolte **Uložit** a zavřete stránku.

### <a name="location-profile"></a>Profil umístění

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. V seznamu profilů polohy vyberte možnost **FLOOR-05**.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Všeobecné** se ujistěte, že jsou obě následující možnosti nastaveny na *Ano*:

    - Povolit položku v umístění
    - Povolit stav umístění

1. Zvolte **Uložit**.

    > [!IMPORTANT]
    > Pokud již možnosti **Povolit položku na místě** a **Povolit stav místa** byly nastaveny na *Ano*, přeskočte na pokyny pro nastavení pevné záložky **Rozměry** v kroku 10. Pokud možnosti ještě nebyly nastaveny na *Ano*, musíte provést kontrolu konzistence modulu **Správa skladu** poté, co je nastavíte ručně. V takovém případě pokračujte dalším krokem.

1. Chcete-li spustit kontrolu konzistence, přejděte na **Správa systému \> Periodické úkoly \> Databáze \> Kontrola konzistence**.
1. V dialogovém okně **Kontrola konzistence** nastavte následující hodnoty:

    - **Modul:** *Řízení skladu*
    - **Kontrola / oprava:** *Kontrola*
    - **Od data:** Toto pole ponechte prázdné.
    - **Kontrola konzistence stavu umístění skladu:** Zaškrtněte toto políčko.

1. Vyberte **OK**.

    > [!TIP]
    > Po dokončení kontroly konzistence se zobrazí oznámení. Otevřete [Centrum akcí](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) pro zobrazení zprávy. Vyberte **Podrobnosti zprávy** k zobrazení podrobností.
    >
    > Pokud se ve zprávě pro kontrolu konzistence uvádí: „Byly nalezeny nesprávné informace o stavu umístění pro umístění XXXX ve skladu XX“, musíte znovu spustit kontrolu konzistence. Tentokrát nastavte **Kontrola / oprava** na *Opravit chybu*. Zobrazte zprávy a ujistěte se, že nebyly nalezeny žádné chyby.

1. Nyní musíte dokončit nastavení profilu místa. Přejděte zpět na **Správa skladu \> Nastavení \> Sklad \> Profily umístění**, vyberte profil místa **FLOOR-05** a poté V podokně Akcí vyberte **Upravit**.
1. Na záložce s náhledem **Rozměry** nastavte následující hodnoty:

    - **Procento využití objemu:** *100*
    - **Objemová metoda použitá pro umístění zásob:** *Použijte objem místa*
    - **Skutečná výška skladového místa:** *10*
    - **Skutečná šířka skladového místa:** *10*
    - **Skutečná hloubka skladového místa:** *10*
    - **Maximální hmotnost:** *100*

1. Zvolte **Uložit**.

### <a name="mobile-device-menu-items"></a>Položky nabídky mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se položka nabídky k třídění.
1. V záhlaví nastavte následující hodnoty:

    - **Název položky nabídky:** *Nastavit*
    - **Titul:** *Nastavit*
    - **Režim:** *Práce*
    - **Použít existující práci:** *Ne*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Proces tvorby práce:** *Nastavit*
    - **Typy úprav zásob:** *Nastavit*

1. Zvolte **Uložit**.

### <a name="mobile-device-menu"></a>Nabídka mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V seznamu nabídek vyberte možnost **Zásoby**.
1. V podokně akcí vyberte **Upravit**.
1. V seznamu **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky **Upravit**.
1. Stisknutím tlačítka se šipkou doprava přesuňte **Upravit** do seznamu **Struktura nabídky**. Tímto způsobem se přidá nová položka nabídky do vybrané nabídky.
1. Zvolte **Uložit**.

### <a name="movement-types"></a>Typy pohybů

1. Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Typy pohybů**.
1. V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:

    - **Kód typu pohybu:** *KONSOLIDOVAT*
    - **Popis:** *Konsolidovat místa*
    - **ID pracovní třídy:** *InvMov*

1. Zvolte **Uložit**.

## <a name="example-scenario"></a>Příklad

Následující scénář používá k vytvoření inventáře aplikaci skladu na mobilním zařízení pro *úpravu* zásob do dvou míst ve skladu.

### <a name="add-inventory-to-locations"></a>Přidat zásoby na skladová místa

1. Přihlaste se do mobilního zařízení jako uživatel, který je nastaven pro sklad *51*.
1. Přejděte na **Zásoby \> Upravit**.

    Nyní zadáte první úpravu místa.

1. V úloze **Úprava** vyberte místo, pro které chcete provést úpravu zásob. V poli **LOC** vyberte *LP-001*.
1. Potvrďte umístění.
1. Vytvořte ID registrační značky pro položku, která bude přidána do umístění. Do pole **LP** zadejte hodnotu *LP00101*.
1. Potvrďte registrační značku.
1. Zadejte položku, která bude přidána na registrační značku. Do pole **ITEM** zadejte hodnotu *M9201*.
1. Potvrďte položku.
1. Zadejte množství položky, která bude přidána. Do pole **QTY** zadejte *10*.
1. Potvrďte množství.

    Zobrazí se zpráva „Práce dokončena“. Nyní zadáte druhou úpravu místa.

1. V úloze **Úprava** vyberte místo, pro které chcete provést úpravu zásob. V poli **LOC** vyberte *LP-002*.
1. Potvrďte umístění.
1. Vytvořte ID registrační značky pro položku, která bude přidána do umístění. Do pole **LP** zadejte hodnotu *LP00201*.
1. Potvrďte registrační značku.
1. Zadejte položku, která bude přidána na registrační značku. Do pole **ITEM** zadejte hodnotu *M9201*.
1. Potvrďte položku.
1. Zadejte množství položky, která bude přidána. Do pole **QTY** zadejte *15*.
1. Potvrďte množství.

    Zobrazí se zpráva „Práce dokončena“.

1. Stiskněte tlačítko nabídky (tzv. „hamburgerové tlačítko“ nebo „hamburger“) a vyberte **Storno**, chcete-li opustit úkol **Úprava**.

### <a name="consolidate-locations"></a>Konsolidovat umístění

1. Přejděte na **Správa skladu \> Periodické úkoly \> Konsolidace položek**.
1. V záhlaví vyberte sklad, pro který chcete provést konsolidaci. V poli **Sklad** zadejte *51*.

    Záznam se zobrazuje pro každé místo, kde byla položka *M9201* upravena. Sloupec **Procento využití** ukazuje objemové využití každého místa.

1. Chcete-li konsolidovat inventář, vyberte všechna umístění, která musí být konsolidována, a poté na podokně Akce vyberte **Konsolidovat zásoby**.
1. V dialogovém okně **Konsolidovat zásoby** zadejte umístění a typ pohybu, který by měl být použit k vytvoření práce pro přesun zásob. Nastavte následující hodnoty:

    - **Místo:** *LP-001*
    - **Kód typu pohybu:** *KONSOLIDOVAT*

1. Vyberte **OK**.
1. Obdržíte informační zprávu, která ukazuje pohybovou práci, která byla vytvořena. Poznamenejte si ID pohybu práce.

### <a name="view-movement-work"></a>Zobrazit pohybové práce

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Zobrazit vytvořenou práci. Filtrujte nebo prohledávejte pracovní mřížku pomocí ID práce s pohybem z konsolidace zásob.

    V tomto scénáři bylo jako umístění konsolidace zásob použito existující místo se zásobami. Proto bylo vytvořeno pouze jedno ID práce.

    > [!NOTE]
   > Systém vytvoří jedno pracovní ID pro každý pohyb, který musí být dokončen. Pokud určíte místo, které již obsahuje zásoby, vytvoří se pouze jedno ID práce. Pokud zadáte nové místo, vytvoří se dvě ID práce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]