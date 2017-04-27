---
title: "Mobilní pracovní prostor zásob na skladě pro aplikaci Microsoft Dynamics 365 for Operations"
description: "Mobilní pracovní prostor Zásoby na skladě pomáhá získat mobilní přehled o rezervovaných a dostupných zásobách a je k dispozici kdykoli a kdekoli."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilní pracovní prostor zásob na skladě pro aplikaci Microsoft Dynamics 365 for Operations

Mobilní pracovní prostor Zásoby na skladě pomáhá získat mobilní přehled o rezervovaných a dostupných zásobách a je k dispozici kdykoli a kdekoli. 

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                         | popis                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Přečtěte si o mobilní platformě Microsoft Dynamics 365 for Operations | [Mobilní platforma Microsoft Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Prostředí, které má Microsoft Dynamics 365 for Operations verzi 1611 a Microsoft Dynamics for Operations aktualizaci platformy 3 (listopad 2016) |
| Oprava KB 3215650                                                    | Nainstalujte opravu hotfix, abyste povolili pracovní prostory, které jsou součástí Microsoft Dynamics 365 for Operations.                                       |
| Mobilní zařízení, které má nainstalovanou aplikaci Dynamics 365 for Operations | Stáhněte aplikaci Dynamics 365 for Operations z vašeho obchodu mobilních aplikací.                                                                           |

## <a name="introduction"></a>Úvod
Firmy mají obvykle více dodávek a příjmů zásob každý den. Tyto pohyby neustále mění stav zásob na skladě. Mobilní centrum zásob na skladě umožňuje zobrazit stav zásob na skladě společnosti tak, aby bylo možné získat nejnovější přehled o skladových zásobách na mobilních zařízeních podle vašeho výběru. Bez ohledu na to, zda pracujete ve skladu, nákupu, prodeji, výrobě nebo řízení nebo mají jiné role, můžete přistupovat k datům na skladě kdykoli a kdekoli. Mobilní pracovní prostor poskytuje okamžitý přehled o stavu zásob v rámci zařízení a umožňuje zobrazit zásoby na skladě na různých zařízeních, aktuální rezervace a nerezervované množství zásob na skladě. Můžete také zadat čísla zboží k dotazování množství na skladě a provést filtrované vyhledávání produktů na skladě nebo variant. Mobilní pracovní prostor konkrétně poskytuje následující funkce:

-   Můžete vyhledávat podle čísla produktu nebo názvu produktu k zobrazení stavu zásob na skladě.
-   U vybraných produktů můžete zobrazit následující informace:
    -   Zásoby na skladě podle pracoviště
    -   Množství zásob podle skladu
    -   Zásoby na skladě podle pracoviště
    -   Zásoby na skladě podle šarže (pro kontrolované šarže produktů)
    -   Zásoby na skladě podle stavu zásob

<!-- -->

-   Zásoby na skladě produktu jsou zobrazeny následujícím způsobem:
    -   Podle fyzické inventury (Toto zobrazení představuje celkovou částku).
    -   Podle fyzické rezervy (Toto zobrazení představuje rezervovanou částku).
    -   Fyzicky k dispozici (Toto zobrazení představuje částku k dispozici, která nemá žádné rezervace.)

## <a name="get-started"></a>Začínáme
Chcete-li začít pracovat v mobilním zařízení:

1.  Stáhněte aplikaci Microsoft Dynamics 365 for Operations z vašeho obchodu mobilních aplikací.
2.  Spusťte aplikaci na svém zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte společnost, do které se chcete přihlásit. Například zadejte **USMF**.
5.  Při prvním přihlášení budete vyzváni k zadání uživatelského jména a hesla pro váš účet aplikace Microsoft Dynamics 365 for Operations. Zadejte své přihlašovací údaje. Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.

Pro zobrazení pracovního prostoru ve své mobilní aplikaci musíte nejprve publikovat požadovaný pracovní prostor do aplikace Dynamics 365 for Operations.

1.  Spusťte aplikaci Dynamics 365 for Operations.
2.  Přejděte do nabídky **Správa systému** &gt; **Nastavení** &gt; **systémových parametrů**.
3.  Zvolte **Spravovat aplikaci pro mobilní zařízení**.
4.  Vyberte pracovní prostor pro publikování na mobilní platformu.
5.  Vyberte **Publikovat pracovní prostor**.
6.  Aktualizujte zařízení pro zobrazení publikovaných pracovních prostorů.

## <a name="view-the-onhand-inventory-for-a-product"></a>Zobrazení zásob na skladě pro vybraný produkt
1.  Na svém mobilním zařízení vyberte pracovní prostor **Zásoby na skladě**.
2.  Vyberte **Kontrola zásob na skladě pro položku**. Zobrazí se seznam produktů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale tuto hodnotu můžete změnit. Další informace naleznete v příručce pro předběžné načtení.
3.  Pokud položka není v seznamu uvedena, vyberte **Hledat více**, chcete-li provést online hledat v Dynamics 365 for Operations. Vyhledávejte podle čísla produktu nebo přepněte do vyhledávání podle názvu produktu.
4.  Vyberte produkt. Pokud položka obsahuje obrázek, obrázek je zobrazen.
5.  Vyberte jednu z následujících možností k zobrazení stavu zásob na skladě:
    -   Zobrazení zásob na skladě podle pracoviště
    -   Zobrazení zásob na skladě podle skladu
    -   Zobrazení zásob na skladě podle místa
    -   Zobrazení zásob na skladě podle šarže (pro kontrolované šarže produktů)
    -   Zobrazení zásob na skladě podle zboží

    Zásoby na skladě produktu jsou zobrazeny následujícím způsobem:
    -   Podle fyzické inventury (Toto zobrazení představuje celkovou částku).
    -   Podle fyzické rezervy (Toto zobrazení představuje rezervovanou částku).
    -   Fyzicky k dispozici (Toto zobrazení představuje částku k dispozici, která nemá žádné rezervace.)




