---
title: Uživatelská nastavení mobilního zařízení
description: Toto téma vysvětluje, jak spravovat uživatelské nastavení mobilních zařízení pro pracovníky skladu.
author: Mirzaab
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 13c99854224a6d220e73a43636d85ec1951f8149
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901865"
---
# <a name="mobile-device-user-settings"></a>Uživatelská nastavení mobilního zařízení

[!include [banner](../../includes/banner.md)]

Nová mobilní aplikace Warehouse Management má sadu nastavení specifických pro aplikaci, která pomáhají přizpůsobit uživatelské prostředí. Protože aplikaci lze použít na zařízeních různých velikostí a konfigurací obrazovek (například na tabletu, telefonu nebo na ruce), může být užitečné centrálně spravovat tato nastavení z aplikace Microsoft Dynamics 365 Supply Chain Management.

Funkce *uživatelské nastavení mobilního zařízení* umožňuje definovat globální uživatelská nastavení, která budou použita na všech zařízeních. Můžete také definovat podrobnější uživatelské nastavení pro jednotlivé značky zařízení, modely zařízení a/nebo pracovníky. Když se pracovník přihlásí k mobilní aplikaci Warehouse Management, aplikace načte a použije nejkonkrétnější profil nastavení, který je uložen v Supply Chain Management pro odpovídající značku, zařízení nebo ID uživatele.

Tato funkce může pracovníkům pomoci začít rychleji, kdykoli začnou používat nové zařízení. Několik příkladů:

- Správci mohou zavést standardní sadu předvoleb, které nejlépe fungují pro zařízení od konkrétního výrobce a/nebo pro konkrétní modely zařízení. Pracovníci tedy mohou začít s novým zařízením, aniž by museli nutně měnit nastavení.
- Pokud má vaše společnost fond identických zařízení, která jsou sdílena mezi pracovníky, pracovníci uvidí jejich upřednostňované nastavení při každém přihlášení, i když nikdy nepoužili konkrétní fyzické zařízení, které v daný den vybrali.
- V nástroji Supply Chain Management mohou správci zobrazit a upravit všechna uložená nastavení, a to i pro jednotlivé pracovníky. Tato funkce jim může pomoci při odstraňování problémů nebo dolaďování nových funkcí.

> [!IMPORTANT]
> Funkce *Uživatelské nastavení mobilního zařízení* se vztahuje pouze na novou mobilní aplikaci Warehouse Management. Se starou aplikací skladu to nefunguje.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Zapněte funkci uživatelského nastavení mobilního zařízení

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Uživatelská nastavení, ikony a názvy kroků pro novou aplikaci skladu*

## <a name="create-and-manage-user-settings"></a>Vytváření a správa uživatelských nastavení

Použijte stránku **Uživatelské nastavení mobilního zařízení** k vytvoření, zobrazení a správě profilů nastavení na všech úrovních podrobností. Když pracovník poprvé upraví své uživatelské nastavení na novém zařízení, automaticky se na tuto stránku přidá nový profil, pokud ještě neexistuje. Tento profil se poté aktualizuje pokaždé, když pracovník provede změnu.

Můžete také definovat profil nastavení, který platí pro všechny značky zařízení, modely zařízení a/nebo pracovníky. Poté můžete zvýšit podrobnosti použitím konkrétnějších nastavení pro jednotlivé značky, modely nebo pracovníky.

Podle těchto pokynů můžete vytvořit a spravovat uživatelské nastavení svých mobilních zařízení.

1. Přejděte na **Warehouse Management \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. Vyberte existující profil nastavení uživatele v podokně seznamu a otevřete jeho záznam. Případně vyberte **Nový** v podokně akcí a vytvořte nový profil.

    Každý profil v podokně seznamu je označen, aby indikoval značku, model nebo ID uživatele, kterého se profil týká. Obecnější profily mají pro některé nebo všechny tyto vlastnosti hodnotu *Všechno*.

1. V části záhlaví záznamu pro nový nebo vybraný profil nastavení nastavte následující pole:

    - **Název značky zařízení** - Vyberte název značky zařízení, na který by se měl profil vztahovat. Pokud by se profil měl vztahovat na všechny značky, nechte toto pole prázdné. Seznam hodnot obsahuje všechny značky definované v systému. Informace o tom, jak definovat seznam značek, najdete v další části.
    - **ID modelu zařízení** - Vyberte model zařízení, na který by se měl profil vztahovat. Pokud by se profil měl vztahovat na všechny modely vybrané značky, nechte toto pole prázdné. Seznam hodnot zahrnuje všechny modely, které byly definovány pro značku vybranou v poli **Název značky zařízení**. Informace o tom, jak definovat seznam modelů pro každou značku, najdete v další části.
    - **ID uživatele** - Vyberte ID uživatele skladníka, na kterého by se měl vztahovat profil nastavení. Pokud by se profil měl vztahovat na všechny pracovníky, nechte toto pole prázdné.

1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Pozice tlačítka** – Vyberte, jak mají být umístěna tlačítka na zařízení. Prvky v aplikaci budou přesunuty, aby lépe odpovídaly preferencím nebo preferované ruce pracovníka. Dostupné možnosti jsou *Vpravo dole (výchozí)*, *Vlevo dole*, *Vpravo nahoře* a *Vlevo nahoře*.
    - **Orientace displeje** – Vyberte orientaci displeje, která by měla být v aplikaci použita ve výchozím nastavení.
    - **Skenovat pomocí fotoaparátu** - Nastavte tuto možnost na *Ano*, pokud chcete použít kameru zařízení ke skenování vstupních polí, kde je nastaven preferovaný vstupní režim *snímání*. Pokud má vaše zařízení vestavěný skener, nastavte tuto možnost na *Ne*, aby byl použit skener.
    - **Zobrazit fotografii produktu** - Vyberte, zda se mají zobrazit fotografie produktu, pokud jsou k dispozici pro vydaný produkt. Další informace o tom, jak přidat obrázky produktu, najdete v části [Přidání obrázku k produktu](../pim/tasks/add-image-product.md).
    - **Zobrazit barevný motiv** - Vyberte barevný motiv pro zařízení.
    - **Hladina zvuku** - Vyberte úroveň zvuku pro zařízení. Vyberte hodnotu mezi 0 (nula) a 10. Hodnota *0* nepředstavuje žádný zvuk a hodnota *10* představuje maximální hlasitost. Výchozí hodnota je *4*.
    - **Úroveň vibrací** - Vyberte úroveň vibrací pro zařízení. Vyberte hodnotu mezi 0 (nula) a 5. Hodnota *0* nepředstavuje žádné vibrace a hodnota *5* představuje maximální vibrace. Výchozí hodnota je *1*.
    - **Procento měřítka textu** - Určete velikost textu jako procento standardní velikosti. Zadejte hodnotu mezi 70 a 400. Hodnota *70* představuje nejmenší měřítko textu a hodnota *400* představuje největší měřítko textu. Výchozí hodnota je *100*.
    - **Procento měřítka tlačítka** - Určete velikost tlačítka jako procento standardní velikosti. Zadejte hodnotu mezi 50 a 200. Hodnota *50* představuje nejmenší měřítko tlačítka a hodnota *200* představuje největší měřítko tlačítka. Výchozí hodnota je *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Vytváření a správa značek mobilních zařízení

Použijte stránku **Značky mobilních zařízení** k zobrazení, vytvoření a správu značek a modelů zařízení, které lze použít s vašimi profily nastavení. Mobilní aplikace automaticky načte a odešle místní název značky a ID modelu, když pracovník poprvé upraví nastavení na daném zařízení. Většina z těchto záznamů bude proto obvykle generována automaticky. Můžete však také spravovat všechny záznamy na této stránce. Například můžete každé značce a modelu poskytnout užitečnější popisy, které vám pomohou rozlišit ID podobných nebo kryptických modelů.

Podle těchto pokynů můžete vytvořit a spravovat značky a modely svých mobilních zařízení.

1. Přejděte do **Warehouse Management \> Nastavení \> Mobilní zařízení \> Značky mobilního zařízení**.
1. V podokně seznamu vyberte značku mobilního zařízení pro otevření jejího záznamu. Případně vyberte **Nový** v podokně akcí a vytvořte novou značku.
1. V části záhlaví záznamu pro novou nebo vybranou značku zařízení nastavte následující pole:

    - **Název značky zařízení** - Značka zařízení, například *Microsoft Corporation*.
    - **Popis** - Můžete zadat popis, který vám pomůže rozlišit názvy značek.

1. Záložka s náhledem **Modely mobilních zařízení** zobrazuje všechny modely pro vybranou značku zařízení. Tlačítka na panelu nástrojů používejte k přidání řádků do mřížky nebo odstranění řádků. Pro každý řádek můžete nastavit následující pole:

    - **ID modelu zařízení** - ID modelu zařízení, například *Surface Book 2*.
    - **Popis** - Můžete zadat popis, který vám pomůže rozlišit ID modelů.

## <a name="additional-resources"></a>Další prostředky

- [Instalace a připojení mobilní aplikace Řízení skladu](install-configure-warehouse-management-app.md)
- [Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management](step-icons-titles.md)