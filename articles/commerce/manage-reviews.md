---
title: Správa hodnocení a recenzí
description: V tomto článku je vysvětleno, jak spravovat hodnocení a recenze v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79738030d4e33ceaad105a404b8188384d5a320c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881316"
---
# <a name="manage-ratings-and-reviews"></a>Správa hodnocení a recenzí

[!include [banner](includes/banner.md)]

V tomto článku je vysvětleno, jak spravovat hodnocení a recenze v konfigurátoru webu Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce použije Microsoft Azure Cognitive Service k automatickému moderování recenzí pomocí redigování slov. Kromě toho mohou moderátoři použít konfigurátor webu Dynamics 365 Commerce k implementaci následujících ručních úkolů:

- Moderování recenzí tím, že na ně odpovíte nebo je odeberete.
- Odstranění recenzí zákazníka na žádost zákazníka.
- Hromadný import hodnocení a recenzí pro všechny produkty do šablony Microsoft Power BI, aby bylo možné analyzovat trendy hodnocení a recenzí.

## <a name="read-a-review"></a>Přečíst recenzi 

Pokud si chcete přečíst recenzi v konfigurátoru webu v Commerce, postupujte následovně.

1. Přejděte na **Domů \> Recenze \> Moderování**.
1. Pomocí vyhledávacího pole v pravém horním rohu stránky můžete filtrovat recenze, které jsou zobrazeny podle ID produktu, názvu produktu nebo textu recenze.

Další filtry umožňují omezit recenze podle období, hodnocení, kanálu nebo stavu sledování (přijaté, zodpovězené nebo nahlášené).

![Domovská stránka moderování.](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Odpověď na recenzi 

V některých případech zákazníci, kteří nakoupili produkt, vyjádřili pokojenost nebo nespokojenosti, nebo neznají způsob používání produktu. Jako moderátor můžete odeslat odpověď na recenzi. Tato odpověď se zobrazí spolu s recenzí na webu. 

Pokud chcete odpovědět na recenzi v konfigurátoru webu v Commerce, postupujte následovně.

1. Přejděte na **Domů \> Recenze \> Moderování**.
1. Najít a vybrat revizi, která vyžaduje odpověď.
1. V podokně vlastnosti vpravo vyberte možnost **přidat odpověď.**
1. Zadejte text odpovědi a název, který má být zobrazen pro respondenta. Výchozí název respondenta je **Moderátor**.
1. Po dokončení zvolte **Odeslat odpověď**.

![Odpověď na recenzi.](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Odstranění recenze 

Někdy existuje důvod, proč moderátoři z obchodních důvodů odstraní recenze zákazníků. 

Pokud chcete odstranit recenzi v konfigurátoru webu v Commerce, postupujte následovně.

1. Přejděte na **Domů \> Recenze \> Moderování**.
1. Vyhledejte a vyberte recenzi, kterou je třeba odstranit.
1. V podokně vlastnosti napravo vyberte důvod odstranění v části **Odstranění recenze** a poté vyberte možnost **Odebrat**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Odstranění recenzí zákazníka na žádost zákazníka. 

Někdy si zákazníci přejí, aby jejich hodnocení a recenze byly trvale smazány z webové stránky elektronického obchodu. Moderátor, který obdrží požadavek na odebrání od zákazníka, může odebrat data odběratele pomocí funkce kontroly odstranění. Chcete-li vyhledat a odstranit data odběratele, moderátor potřebuje e-mailovou adresu, kterou odběratel používá k přihlášení a poskytnutí recenzí. 

Chcete-li vyhledat a odstranit data o odběrateli v konfigurátoru webu v Commerce, postupujte následujícím způsobem.

1. Přejděte na **Domů \> Recenze \> Odstranit**.
1. V okně **Hledat uživatele podle e-mailové adresy** zadejte e-mailovou adresu odběratele a pak vyberte **hledat**.
1. Pokud má zákazník nějakou aktivitu týkající se recenzí (např. podání recenze, hlasování o užitečnosti recenzí jiného zákazníka nebo komentáře o recenzi jiného zákazníka), zobrazí se výsledky. Pro každou položku existuje tlačítko **odstranit.**
1. Pro každou položku, kterou je třeba odstranit, vyberte možnost **Odstranit**. Po zobrazení výzvy k potvrzení vyberte možnost **Ano.** 
    
![Odstranění dat zákazníků.](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Může trvat až sedm dní, než budou data zcela odstraněna ze systému. Moderátoři by měli informovat zákazníky o této prodlevě.
> - Pokud uživatelé změnili své jméno v nastavení účtu, může se ve výsledcích hledání zobrazit více položek. V takovém přípdě, chcete-li data zákazníka zcela odstranit, musí moderátor pro každou položku vybrat možnost **Odstranit**. 

## <a name="download-ratings-and-reviews-data"></a>Stáhnout data hodnocení a recenzí

Konfigurátor webu v Commerce umožňuje moderátorům importovat hodnocení a recenzovat data hromadně, aby mohli analyzovat trendy. K dispozici je šablona Power BI, která obsahuje základní metriky. Moderátoři mohou tuto šablonu použít k připojení hromadně importovaných dat a k zobrazení řídicího panelu. Nemusí vytvářet vlastní řídicí panel. Moderátoři mohou také upravit šablonu Power BI tak, aby vyhovovala jejich specifickým potřebám. 

Chcete-li stáhnout data hodnocení a recenzí v konfigurátoru webu v Commerce, postupujte následujícím způsobem.

1. Přejděte na **Domů \> Recenze \> Vykazování**.
1. Chcete-li stáhnout data hodnocení a recenzí hromadně ve formátu hodnot oddělených čárkou (CSV), vyberte možnost **Stáhnout data recenzí**.

## <a name="view-ratings-and-reviews-trends"></a>Zobrazení trendů hodnocení a recenzí

Moderátoři mohou stáhnout šablonu Power BI, aby mohli sledovat trendy v řídicím panelu.

Chcete-li si zobrazit trendy hodnocení a recenzí v konfigurátoru webu v Commerce, postupujte následujícím způsobem.

1. Přejděte na **Domů \> Recenze \> Vykazování**.
1. Vyberte **Šablonu PowerBI** ke stažení šablony.

    ![Stáhnout šablonu Power BI.](media/rnr-moderation-reports.png) 

1. Otevře staženou šablonu pomocí aplikace Power BI. Zavřete dialogové okno **Přístup k webovému obsahu**, které se zobrazí, a poté zavřete zobrazenou chybovou zprávu "Obnovit".
1. Přejděte na **Domovskou stránku**, vberte **Upravit dotazy** a pak vyberte **Nastavení zdroje dat**.
1. V dialogovém okně **Nastavení zdroje dat** vyberte možnost **Změnit zdroj**.
1. V poli **Adresa URL** zadejte cestu k datům recenzí, která jste stáhli v předchozím postupu (například **c:\\reviews\\ReviewsData.csv**).

    ![Pole Adresa URL v dialogovém okně hodnot oddělených čárkou.](media/rnr-powerbi-datasource-settings.png) 

1. Vyberte možnost **OK** a pak zvolte **Použít změny**. Použijete-li změny ve zdroji dat, bude provedena za jednu až dvě minuty.
1. Chcete-li zobrazit hodnocení a recenze trendů, vyberte volbu **List trendů**.

    ![Trendy hodnocení a recenzí.](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Další prostředky

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Konfigurace hodnocení a recenzí](configure-ratings-reviews.md)

[Synchronizace hodnocení produktů v Dynamics 365 Retail](sync-product-ratings.md)

[Povolit ruční publikování hodnocení a recenzí moderátorem](manual-publish-rating-reviews.md)

[Import a export hodnocení a recenzí](import-export-reviews.md)

[Konfigurace ověřování mezi službami](service-to-service-auth.md)

[Nejčastější dotazy k hodnocení a recenzím](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
