---
title: "Zásoby na skladě mobilní pracovní prostor pro Microsoft Dynamics 365 pro provoz aplikace"
description: "Zásoby na skladě mobilní centrum pomáhá získat mobilní podstatu skladu rezervované a je k dispozici kdykoli a kdekoli."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 44 - 40
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Zásoby na skladě mobilní pracovní prostor pro Microsoft Dynamics 365 pro provoz aplikace

Zásoby na skladě mobilní centrum pomáhá získat mobilní podstatu skladu rezervované a je k dispozici kdykoli a kdekoli. 

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                         | popis                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Přečtěte si informace o Microsoft Dynamics 365 pro provoz mobilní platformu | [Dynamics 365 pro mobilní platformu operace](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 pro operace                                          | Prostředí, které má Microsoft Dynamics 365 pro verzi operace 1611 a Microsoft Dynamics pro operace platformy aktualizace 3 (listopad 2016) |
| Opravy hotfix KB 3215650                                                    | Nainstalujte opravu hotfix Chcete-li povolit pracovní prostory, které jsou součástí aplikace Microsoft Dynamics 365 pro operace.                                       |
| Mobilní zařízení, které má 365 Dynamics pro operace aplikace nainstalována | Stáhněte 365 Dynamics pro operace aplikace z úložiště vaše mobilní aplikace.                                                                           |

## <a name="introduction"></a>Úvod
Firmy mají obvykle více dodávky a příjmy více zásob každý den. Tyto pohyby neustále změna stavu zásob na skladě. Mobilní centrum zásob na skladě umožňuje zobrazit stav zásob na skladě společnost tak, aby bylo možné získat nejnovější poznatky do skladu dat na mobilních zařízeních podle svého výběru. Bez ohledu na to, zda pracovat skladu, nákupu, prodeje, výroby a řízení nebo mají jiné role můžete přístup k datům na skladě kdykoli a kdekoli. Mobilní pracovní prostor poskytuje okamžitý přehled o stavu zásob v rámci zařízení a umožňuje zobrazení různých zařízení, aktuální rezervace materiálu a množství zásob na skladě na skladě. Můžete zadat čísla zboží na dotaz množství na skladě a filtrované vyhledávání produktů na skladě nebo varianty. Mobilní pracovní prostor konkrétně poskytuje následující funkce:

-   Můžete vyhledávat podle čísla produktu nebo název produktu můžete nalézt produkty zobrazit stav zásob na skladě.
-   U vybraných produktů můžete zobrazit následující informace:
    -   Na skladě pro každý server
    -   Na skladě podle skladu
    -   Na skladě dle lokace
    -   Na skladě pro šarži (pro kontrolované šarže produktů)
    -   Na skladě dle stavu skladu

<!-- -->

-   Zásoby na skladě produktu je zobrazen následujícím způsobem:
    -   Podle fyzické inventury (Toto zobrazení představuje celkovou částku).
    -   Ve vyhrazené fyzické (Toto zobrazení představuje vyhrazené částky).
    -   Ve fyzicky k dispozici (Toto zobrazení představuje k dispozici částku, která nemá žádné výhrady.)

## <a name="get-started"></a>Začínáme
Chcete-li začít pracovat v mobilním zařízení:

1.  Z úložiště mobilní aplikace stáhněte a nainstalujte 365 Microsoft Dynamics pro operace app.
2.  Spuštění aplikace v zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte přihlášení do společnosti. Například zadejte **USMF**.
5.  Při prvním přihlášení, budete vyzváni pro uživatelské jméno a heslo pro vaše 365 Microsoft Dynamics pro účet operací. Zadejte svá pověření. Po přihlášení, zobrazí se dostupné pracovní prostory pro vaši firmu.

Zobrazení pracovní plochy na mobilní aplikace, musíte nejprve publikovat požadované pracovní prostory do 365 Dynamics pro operace app.

1.  Spusťte Dynamics 365 pro operace.
2.  Přejít na **Správa systému**&gt;**nastavení**&gt;**parametry systému**.
3.  Vyberte **Správa mobilní aplikace**.
4.  Vyberte pracovní prostor k publikování na mobilní platformy.
5.  Vyberte **publikovat pracovního prostoru**.
6.  Aktualizujte zařízení zobrazit publikované pracovní prostory.

## <a name="view-the-onhand-inventory-for-a-product"></a>Zobrazení množství na skladě zásob produktu
1.  V mobilním zařízení, vyberte **na skladě** prostoru.
2.  Vyberte **kontrola na skladě pro položku**. Zobrazí se seznam produktů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení jsou načteny 50 položek, ale tuto hodnotu můžete změnit. Další informace naleznete v tématu Příručka předem čtení.
3.  Pokud položka není v seznamu uveden, vyberte **hledat více** Chcete-li provést online hledat v Dynamics 365 pro operace. Hledání podle čísla produktu nebo přepněte do vyhledávání podle názvu produktu.
4.  Vyberte produkt. Pokud položka obsahuje obrázek, obrázek je zobrazen.
5.  Vyberte jednu z následujících možností zobrazíte stav zásob na skladě:
    -   Zobrazení množství na skladě podle webu
    -   Zobrazení množství na skladě podle skladu
    -   Zobrazení množství na skladě podle umístění
    -   Zobrazení množství na skladě pro šarži (pro kontrolované šarže produktů)
    -   Zobrazení množství na skladě dle stavu skladu

    Zásoby na skladě produktu je zobrazen následujícím způsobem:
    -   Podle fyzické inventury (Toto zobrazení představuje celkovou částku).
    -   Ve vyhrazené fyzické (Toto zobrazení představuje vyhrazené částky).
    -   Ve fyzicky k dispozici (v tomto zobrazení představuje částku k dispozici žádné výhrady.)




