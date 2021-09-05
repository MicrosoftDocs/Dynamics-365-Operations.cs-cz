---
title: Přiznání ke srážkové dani pro Egypt
description: Toto téma vysvětluje, jak nakonfigurovat a vygenerovat přiznání ke srážkové dani pro Egypt.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8d78af13e0b3879afd0b6dae7b1a9ece651c3fd2
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403882"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Přiznání ke srážkové dani pro Egypt (EG-00005)

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Přehled
Toto téma vysvětluje, jak nastavit a generovat prohlášení o srážkové dani a formuláře 41 a 11 přiznání ke srážkové dani pro právnické osoby v Egyptě 

Všechny egyptské subjekty musí připravit formulář 41, který shrnuje všechny daně zadržené od místních dodavatelů a poskytovatelů služeb. Kromě formuláře 41 musí být generován formulář 11, který podrobně popisuje všechny zadržené daně od zahraničních poskytovatelů. 

Sestava **Přiznání ke srážkové dani** v Dynamics 365 Finance zahrnuje následující sestavy:

- Formulář přiznání č. 41
- Formulář přiznání č. 11
    
    
## <a name="prerequisites"></a>Předpoklady
Primární adresa právnické osoby musí být v Egyptě.
V pracovním prostoru **Správa funkcí** musí být zapnutá následující funkce:

   - **Globální srážková daň**

Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. Přejděte na **Daň** > **Nastavení** > **Parametry** > **Parametry hlavní knihy** a poté na kartě **Srážková daň** nastavte možnost **Povolit globální srážkovou** daň na **Ano**.
2. V pracovním prostoru **Elektronické přiznání** importujte z úložiště následující formáty elektronického hlášení:

    - Přiznání k WHT Excel (EG)

    > [!NOTE]
    > Výše uvedený formát je založen na **Modelu daňového přiznání** a používá **Mapování modelu daňového přiznání**. Tato další konfigurace bude automaticky importována.

Další informace o tom, jak importovat konfigurace elektronických sestav, najdete v části [Stažení konfigurací elektronických sestav ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Stažení konfigurací elektronického výkaznictví

Implementace formulářů přiznání k WHT pro Egypt je založena na konfiguracích elektronických přiznání (ER). Další informace o možnostech a konceptech konfigurovatelných sestav najdete v tématu [Elektronické přiznání](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Prostředí produkčního a uživatelského akceptačního testování (UAT) najdete v pokynech v tématu [Stáhnout konfiguraci elektronických zpráv ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Chcete-li vygenerovat přiznání ke srážkové dani v egyptské právnické osobě, musíte nahrát následující konfigurace:

- Daňové přiznání model.version.82.xml nebo novější verze
- Daňové přiznání model mapping.version.82.133.xml nebo novější verze
- Přiznání k WHT Excel (EG).version.82.21 nebo novější verze

Po stažení konfigurací ER ze služby Lifecycle Services (LCS) nebo z globálního úložiště proveďte následující kroky.

1. Přejděte do pracovního prostoru **Elektronické výkaznictví** a vyberte dlaždici **Konfigurace výkaznictví**.
1. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange > Načíst ze souboru XML**.
1. Nahrajte všechny soubory v pořadí, v jakém jsou uvedeny v předchozích odrážkách. Po načtení všech konfigurací bude v aplikaci Finance uveden konfigurační strom.

## <a name="set-up-application-specific-parameters"></a>Nastavení parametrů pro konkrétní aplikaci

Možnost parametrů specifických pro aplikaci umožňuje uživatelům stanovit kritéria, jak budou daňové transakce klasifikovány a počítány v každém řádku generovaného přehledu v závislosti na konfiguraci **skupina položek srážkové daně** nebo jiných kritériích stanovená v definici vyhledávání.

Formulář 41 prohlášení o srážkové dani obsahuje zvláštní sloupec, kde musí být transakce srážkové daně klasifikována v souladu s pojmenovanou klasifikací daňového úřadu **Typ slevového kódu**. Namísto zahrnutí těchto nových klasifikací jako nových vstupních údajů při zaúčtování transakcí bude klasifikace určena na základě různých vyhledávání zavedených v nabídce **Konfigurace** > **Nastavit parametry specifické pro aplikaci** > **Nastavit** za účelem splnění požadavků přiznání ke srážkové dani pro Egypt. 

Následující konfigurace se používá ke klasifikaci transakcí v sestavě formuláře přiznání ke srážkové dani 41:

- **DiscountTaxTypeLookup** -> Sloupec č. 18 

Pomocí následujících kroků můžete nastavit různá vyhledávání použitá ke generování přiznání k WHT a souvisejících účetních výkazů. 

1. V pracovním prostoru **Elektronické přiznání** vyberte **Konfigurace** > **Nastavení** k nastavení pravidel klasifikace transakcí v sestavě přiznání k WHT. 
2. Vyberte aktuální verzi a na kartě s náhledem **Vyhledávání** vyberte název vyhledávání. Například **DiscountTaxTypeLookup**. Toto vyhledávání identifikuje seznam typů slev požadovaných daňovým úřadem.
3. Na záložce s náhledem **Podmínky** vyberte **Přidat** a v novém řádku ve sloupci **Výsledek vyhledávání** vyberte související řádek, který představuje klasifikaci ve **sloupci 18**.
4. Ve sloupci **Skupina položek srážkové daně** vyberte související kód, který se používá k identifikaci klasifikace. Například **Povolená sleva**.  
5. Opakujte kroky 3 a 4 pro všechna dostupná vyhledávání.
6. Opět vyberte **Přidat** k zahrnutí závěrečného řádku záznamu a ve sloupci **Výsledek vyhledávání** vyberte **Nelze použít**. 
7. Ve zbývajících sloupcích vyberte **Není prázdné**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Nastavení parametrů hlavní knihy

Chcete-li vygenerovat hlášení formuláře přiznání k WHT v Microsoft Excel, definujte formát ER na stránce **Obecné parametry hlavní knihy**.

1. Přejděte na **Daň** > **Nastavení** > **Parametry hlavní knihy**.
2. Na kartě **Srážková daň** v poli **Mapování formát přiznání k WHT** vyberte **Přiznání k WHT Excel (EG)**. Pokud toto pole necháte prázdné, vygeneruje se standardní hlášení o DPH ve formátu SSRS.


![Formulář přiznání.](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Vygenerování formulářů přiznání ke srážkové dani
Proces přípravy a odeslání formuláře přiznání ke srážkové dani pro konkrétní období je založen na transakcích srážkové daně zaúčtovaných během úlohy vypořádání a platby daně. Další informace o globální srážkové dani viz [Globální srážková daň](../general-ledger/global-withholding-tax-overview.md).

Chcete-li vygenerovat zprávu o daňovém přiznání, proveďte následující kroky.

1. Přejděte do nabídky **Daň** > **Přiznání** > **Srážková daň** > **Platba srážkové daně*.
2. Vyberte zúčtovací období a poté vyberte datum od pro zprávu. 
3. Zadejte datum transakce a poté vyberte **OK**.
4. V dialogovém okně, které se otevře, vyberte jeden nebo více typů formulářů **Formulář č. 41**, **Formulář č. 11** nebo **Žádný**. Pokud vyberete **Žádný**, je generována standardní sestava. 
5. Vyberte jazyk. Všechny sestavy jsou přeloženy do **en-us** a **ar-eg**.
6. Zadejte pobočku a název banky, kde bude zaplacena daň.
7. Vyberte typ firmy a poté zadejte čísla šeků a dokladů. 
8. Zadejte typ entity. 
9. Zadejte jméno registrované osoby pro přiřazení formuláře a vyberte **OK** pro potvrzení generování sestavy. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
