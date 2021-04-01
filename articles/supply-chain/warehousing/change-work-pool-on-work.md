---
title: Změnit fond práce u práce
description: Toto téma vysvětluje, jak můžete pomocí tlačítka Změnit fond práce pro pracovní položky změnit fond práce stávající práce.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 61b988cf2501812e940f726e02d8fc1bcee2c035
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233048"
---
# <a name="change-work-pool-on-work"></a>Změnit fond práce u práce

[!include [banner](../includes/banner.md)]

Fondy práce můžete použít k uspořádání práce do skupin. Můžete například vytvořit fond práce pro klasifikaci práce, ke které dochází v určitém skladovém místě.

Funkce *Změna fondu práce v práci* přidá tlačítko **Změna fondu práce** do podokna akcí pro pracovní položky. Proto mohou vedoucí skladu snadno změnit fond práce stávající práce. Tato funkce umožňuje manažerům rychle reagovat na změny ve skladu ve skladu a pomáhá zlepšit jejich schopnost přizpůsobit se měnícím se situacím a potřebě převést práci do jiného pracovního fondu.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Zapněte funkci Změnit fond práce pro práci

Než začnete tuto funkci nastavovat nebo používat, musíte se ujistit, že je ve vašem systému k dispozici. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Změnit fond práce pro práci*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Nastavte funkci Změnit fond práce pro práci

Chcete-li tuto funkci používat, musíte mít nastaveny některé fondy práce. Můžete také nastavit své pracovní šablony, aby automaticky přiřadily fond. Pokud chcete využít scénář uvedený v tomto tématu jako příklad, nastavte systém podle popisu v této části.

### <a name="set-up-work-pools"></a>Nastavení fondů práce

Fondy práce umožňují organizovat pracovní položky podle typu. Chcete-li pracovat s funkcí *Změna fondu práce pro práci*, musíte mít k dispozici alespoň dva fondy práce. Chcete-li zobrazit a přidat fondy práce, postupujte podle těchto kroků.

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Fondy práce**.
1. Pokud pracujete s demo daty společnosti **USMF** a budete pokračovat v příkladu scénáře dále v tomto tématu, přidejte dva fondy práce, které mají následující nastavení:

    - Fond práce 1:

        - **ID fondu práce:** *Webshop*
        - **Popis:** *Webový obchod*

    - Fond práce 2:

        - **ID fondu práce:** *CallCenter*
        - **Popis:** *Kontaktní středisko*

1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-work-templates"></a>Nastavit šablony práce

Pro každou ze svých pracovních šablon můžete podle potřeby nastavit výchozí fond práce. Pro každou příslušnou šablonu přiřadíte fond práce ve sloupci **ID fondu práce**. V tomto případě všechny pracovní položky, které jsou generovány pomocí dané šablony, automaticky zdědí přiřazený fond práce. Pokud pracujete s demo daty společnosti **USMF** a budete pokračovat v příkladu scénáře dále v tomto tématu, postupujte podle následujících kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V podokně Akce vyberte možnost **Upravit**, tím přepnete stránku režimu úprav.
1. Upravte šablonu nastavením následujících hodnot:

    - **Pracovní šablona:** *62 výdejů do balení*
    - **ID fondu práce:** *Webshop*

1. Zvolte **Uložit**.

## <a name="example-scenario"></a>Příklad

Tento scénář ukazuje, jak změnit tok zpracování pro existující pracovní položku změnou jejího fondu práce. Používá demo data společnosti **USMF** a nastavení, která byla navržena dříve v tomto tématu.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Vytvořte prodejní objednávku a uvolněte ji do skladu

1. Potvrďte, že je k dispozici dostatek zásob na skladě pro položky *A0001* a *A0002* ve skladu *62*. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Seznam na skladě** a upravte filtry podle obrázku:

    - Hodnota **Sklad** začíná na *62*.
    - Hodnota **Číslo položky** je buď *A001* nebo *A002*.

    Demo data by měla množství 10.

    Dále musíte vytvořit prodejní objednávku.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-007*
    - **Sklad:** *62*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *2*

1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.
1. Zavřete stránku.
1. Na záložce s náhledem **Řádky prodejní objednávky** možnost **Přidat řádek**. Přidá se další řádek do vaší prodejní objednávky. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *2*

1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.
1. Zavřete stránku.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.
1. Zobrazí se informační zprávy určující ID vlny a ID dodávky, jež byly vytvořeny z uvolnění. Poznamenejte si ID vlny.

### <a name="review-the-outbound-wave"></a>Zkontrolujte odchozí vlnu

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. V mřížce vyhledejte ID vlny vytvořené uvolněním prodejní objednávky.
1. Chcete-li zobrazit podrobnosti, vyberte ID vlny.
1. Na pevné záložce **Řádky vlny** se ujistěte, že se u prodejní objednávky zobrazuje ID zásilky.

    > [!TIP]
    > Pokud je možnost **Zpracovat vlnu při uvolnění do skladu** nastavena na *Ne* v nastavení šablony přepravní vlny, musíte vlnu ručně zpracovat výběrem **Zpracovat** na kartě **Vlna** v podokně akcí pro vytvoření práce.

1. Ujistěte se, že vlna byla zpracována. Toto zpracování vytvoří požadovanou práci.

### <a name="view-work-details-and-change-the-work-pool"></a>Zobrazit podrobnosti o práci a změnit fond práce

Můžete použít stránku **Podrobnosti o práci** pro zobrazení vytvořené práce a pro správu fondu práce.

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Vyberte řádek právě vytvořené práce. Ve sloupci **Číslo objednávky** se zobrazí číslo prodejní objednávky.

    Pole **ID fondu práce** bude nastaveno na ID fondu práce, které bylo nastaveno v pracovní šabloně.

    > [!TIP]
    > Pokud nevidíte pole **ID fondu práce**, přidejte sloupec do mřížky a poté stránku obnovte.

1. Chcete-li změnit fond práce, který je spojen s ID práce, v podokně akcí na kartě **Práce** vyberte **Změnit ID fondu práce**.
1. V dialogovém okně **Změna fondu práce** na pevné záložce **Parametry** v poli **ID fondu práce** vyberte pole *CallCenter*.
1. Vyberte **OK** pro použití změn.
1. Všimněte si, že hodnota pole **ID fondu práce** byla nyní změněna na *CallCenter*.

> [!IMPORTANT]
> Když se objeví dialogové okno **Změna fondu práce**, pole **ID fondu práce** může být ve výchozím nastavení prázdné. Pokud je pole prázdné, když vyberete **OK** pro použití změn, odeberete fond práce úplně z práce.
>
> Kromě přepínání fondů práce můžete pomocí tohoto postupu přidat fond práce do jakékoli pracovní položky, která ji nemá, nebo odebrat fond práce z jakékoli pracovní položky, která jej nemá.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]