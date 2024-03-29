---
title: Zobrazení a správa změn adres
description: Tento článek vysvětluje, jak si můžete prohlížet a spravovat změny adres ve službě Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 744ab532fcc663f25ce376817779924bbef15432
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899578"
---
# <a name="view-and-manage-address-changes"></a>Zobrazení a správa změn adres


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek vysvětluje, jak si můžete prohlížet a spravovat změny adres na stránce **Upravit osobní údaje** (kterou otevřete z pracovniho prostoru **Samoobsluha pro zaměstnance**) nebo na stránce podrobností **Pracovník** v Dynamics 365 Human Resources.

Mnoho organizací požaduje, aby zaměstnanci sami spravovali své osobní údaje. Můžete povolit uživatelům aktualizovat svou adresu v **Zaměstnanecká samoobsluha** pracovním prostoru. Poté můžete tyto změny sledovat v **Správa zaměstnanců** pracovním prostoru. Chcete-li použít tuto funkci, musíte určit počet dní, ve kterých chcete zobrazit změny na stránce **Parametry lidských zdrojů**.

## <a name="configure-address-change-parameters"></a>Konfigurace parametrů změny adresy

Chcete-li nakonfigurovat počet dní, kdy se mají změny adresy objevit ve **Správa zaměstnanců** pracovním prostoru, postupujte takto:

1. Na navigačním podokně vyberte **Správa zaměstnanců**.
2. Vybrerte **Odkazy**.
3. Vyberte **Parametry lidských zdrojů**.
4. V **Počet dní** poli pod **Změna adresy** zadejte počet dní, ve kterých se mají změny adresy objevit v **Správa zaměstnanců** pracovním prostoru.
5. Zavřete stránku.

## <a name="create-or-change-an-employee-address"></a>Vytvořte nebo změňte adresu zaměstnance

Zaměstanci mohou aktualizovat svou adresu v **Samoobsluha pro zaměstance** pracovním prostoru. Při vytváření nového adresáře postupujte takto:

1. Na **domovské** stránce vyberte dlaždici **Samoobsluha pro zaměstnance**.
2. Vyberte možnost **Upravit osobní údaje**.
3. Adresu přidáte výběrem tlačítka **Přidat**. Chcete-li aktualizovat existující adresu, vyberte ji ze seznamu a pak vyberte možnost **Upravit**.
4. Zadejte **Název nebo popis**.
5. Vyberte rozevírací seznam **Účel** a poté vyberte typ adresy.
6. Zadejte **Zemi/oblast**.
7. Zadejte **PSČ**.
8. Zadejte **Ulici**.
9. Zadejte **Město**, **Stát**, a **okres**. Tato pole se obvykle nastavují automaticky na základě pole **PSČ**.
10. Můžete vybrat pole **Hlavní** pro označení primární adresy. Jako primární lze označit pouze jednu adresu. Pokud je jako primární adresa již označena jiná adresa, musíte potvrdit, že ji chcete použít jako primární.
11. Můžete vybrat pole **Soukromá** pro označení soukromé adresy. Tuto adresu mohou zobrazit pouze uživatelé s výslovným povolením k zobrazení informací o soukromé adrese.
12. Vyberte **OK**.

## <a name="create-or-change-a-worker-address"></a>Vytvořte nebo změňte adresu pracovníka

Adresu můžete aktualizovat v **Správa zaměstnanců** pracovním prostoru. Při vytváření nového adresáře postupujte takto:

1. Ve **Správa zaměstnanců** pracovním prostoru vyberte **Odkazy** a poté vyberte **Pracovníci**.
2. Vyberte pracovníka a klikněte na možnost **Adresy**.
3. Adresu přidáte výběrem tlačítka **Přidat**. Chcete-li aktualizovat existující adresu, vyberte ji ze seznamu a pak vyberte možnost **Upravit**.
4. Zadejte **Název nebo popis**.
5. Vyberte rozevírací seznam **Účel** a poté vyberte typ adresy.
6. Zadejte **Zemi/oblast**.
7. Zadejte **PSČ**.
8. Zadejte **Ulici**.
9. Zadejte **Město**, **Stát**, a **okres**. Tato pole se obvykle nastavují automaticky na základě pole **PSČ**.
10. Můžete vybrat pole **Hlavní** pro označení primární adresy. Jako primární lze označit pouze jednu adresu. Pokud je jako primární adresa již označena jiná adresa, musíte potvrdit, že ji chcete použít jako primární.
11. Můžete vybrat pole **Soukromá** pro označení soukromé adresy. Tuto adresu mohou zobrazit pouze uživatelé s výslovným povolením k zobrazení informací o soukromé adrese.
12. Vyberte **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Vytvořte budoucí změnu adresy

V některých případech můžete chtít aktualizovat adresu, která se v budoucnu změní. Například by to bylo užitečné, pokud by se zaměstnanec stěhuje 15. dne následujícího měsíce.

1. Otevřete stránku **Spravovat adresy** výběrem **Další možnosti > Upřesnit** z libovolné adresy.
2. Zvolte **Nový** pro vytvoření nové adresy.
3. Zadejte podrobnosti o adrese.
4. Zvolte pevnou záložku **Obecné**.
5. V poli **Datum platnosti** vyberte datum, odkdy bude nová adresa platná.
6. V poli **Datum konce platnosti** můžete vybrat, odkdy adresa nebude platná.
7. Zavřete stránky.

## <a name="view-and-monitor-address-changes"></a>Zobrazení a sledování změn adres

Pracovníci HR si mohou prohlížet a sledovat změny adres z pracovního prostoru **Správa zaměstnanců**. Chcete-li zobrazit změny adresy, vyberte dlaždici **Správa zaměstnanců** na stránce **Domů**. Adresa se změní na dlaždici v pravém horním rohu. Číslo nad **Změny adresy** ukazuje, ke kolika změnám adresy došlo v počtu dní uvedených na stránce **Parametry lidských zdrojů**. 

Když vyberete **Změny adresy** na nové stránce se zobrazí podrobnosti o všech změnách adresy. Můžete si vybrat **Zahrnout budoucí změny adresy** v pravém horním rohu pro zobrazení změn adresy s budoucím datem.

> [!NOTE]
> Pokud chcete dostávat upozornění nebo e-maily o těchto změnách adresy, můžete vytvořit nové pravidlo upozornění na kartě **Možnosti** v podokně akcí. Další informace o tom, jak vytvářet pravidla upozornění, naleznete v tématu [Vytvoření nových pravidel upozornění](../fin-ops-core/fin-ops/get-started/create-alerts.md).
>
> Pokud chcete nakonfigurovat pracovní postup pro změny adresy, můžete vybrat pravidlo **Odeslat externě** v pravidlu upozornění a poté použít Power Automate ke spuštění obchodní události a konfigurace pracovního postupu. Další informace naleznete v tématu [Upozornění jako obchodní události](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
