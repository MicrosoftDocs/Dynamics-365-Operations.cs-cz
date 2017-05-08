---
title: "Vytvoření katalogu kontaktního střediska"
description: "Tento článek podává přehled procesu vytvoření katalogu pro kontaktní středisko."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 857d280ab6d846c19102dd053a2c5f27fe14654c
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-call-center-catalog"></a>Vytvoření katalogu kontaktního střediska

[!include[banner](includes/banner.md)]


Tento článek podává přehled procesu vytvoření katalogu pro kontaktní středisko. 

V kontaktním středisku můžete pomocí katalogů produktů identifikovat produkty, které chcete nabízet odběratelům. Kontaktní střediska obvykle používají tištěné katalogy. Návrhy a výroba tištěného katalogu jsou zpracovány mimo aplikaci Microsoft Dynamics 365 for Operations. Můžete však vytvořit a uložit digitální kopii katalogu v aplikaci Retail and commerce v Dynamics 365 for Operations s použitím stejných formulářů, které slouží k nastavení online maloobchodních katalogů. Před vytvořením katalogu musíte nastavit sortiment produktů a přiřadit sortiment kontaktnímu středisku. Poté přidáte produkty do katalogu výběrem produktů z těchto sortimentů. Poté, co byly produkty přidány do katalogu a katalog je dokončeno, je třeba ověřit katalog pro ověření dat. Poté musíte odeslat katalog ke kontrole a schválení. Po schválení katalogu jej můžete publikovat. Při vytvoření katalogu kontaktního střediska můžete pořídit snímek dat katalogu v době publikování katalogu. Tato funkce snímku vám umožňuje přístup k určité verzi katalogu i v případě, že je katalog později změněn a aktualizován. Katalogy kontaktního střediska lze rovněž nastavit tak, aby obsahovaly následující volitelné prvky.

-   **Zdrojové kódy**: Kódy, které se používají ke sledování reakcí odběratele na konkrétní poštu katalogu.
-   **Produkty zdarma**: Produkty, které jsou zahrnuty do objednávky zákazníka bez dalších příplatků. Tyto produkty jsou přidány do objednávky automaticky při zadání zdrojového kódu katalogu do objednávky.
-   **Skripty**: Texty, které přečte pracovník kontaktního střediska odběrateli při vytváření prodejní objednávky. Skripty mohou zahrnovat pozdravy nebo nákupní návrhy.
-   **Křížový prodej nebo návazný prodej**: Položky, které jsou zobrazeny jako návrh při přidání určitého produktu do objednávky.

Tyto volby se musí nastavit předtím, než je katalog schválen a publikován.

## <a name="prerequisites"></a>Požadavky
Před zahájením tohoto úkolu je nutné dokončit následující úkoly:

-   Nastavte produkty a sortiment produktů.
-   Nastavení maloobchodních produktů.
-   Nastavte sortiment.
-   Vytvořte kontaktní středisko.
-   Nastavte kontaktní centrum.
-   Přidejte kontaktní středisko do organizační hierarchie.
-   Vytvořte nebo upravte organizační hierarchii.

## <a name="create-a-catalog"></a>Vytvoření katalogu
Nejprve musíte vytvořit katalog, přidat produkty do katalogu a následně ověřit a upravit atributy produktů.

## <a name="validate-the-catalog"></a>Ověření katalogu
Po dokončení nastavení katalogu je nutné katalog ověřit. Tento proces ověří, že data, která jsou vyžadována pro atributy kanálu a atributy produktu, jsou úplná a platná a že katalog lze zveřejnit.

## <a name="submit-the-catalog-for-review-and-approval"></a>Odeslání katalogu ke kontrole a schválení
Po ověření katalogu jej můžete odeslat na revizi a schválení. Katalog musí být schválen dříve, než může být publikován. Pracovní postup můžete nakonfigurovat tak, aby katalogy byly automaticky schváleny nebo aby vyžadovaly ruční schválení.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Volitelné: Přidání zdrojových kódů, bezplatných produktů a skriptů
Následující položky lze také přidat do katalogu kontaktního střediska. Tyto položky jsou volitelné.

-   **Zdrojové kódy** mohou společnosti, které poskytují tištěné katalogy, používat ke sledování odezvy odběratelů na konkrétní katalog. Zdrojové kódy se často tisknou na zadní straně katalogu a jsou zadány do prodejní objednávky, když zákazník uskuteční nákup. Zdrojový kód přidáte do katalogu tak, že nejprve vytvoříte cílový trh. Cílový trh je obvykle mapován na vlastní nebo pronajatý seznam poštovních adres.
-   **Bezplatné produkty** jsou propagační položky, které jsou zahrnuty zdarma do objednávky odběratele při odkazování na tento katalog.
-   **Skripty** lze použít při interakci pracovníka se zákazníky v kontextu katalogu nebo produktu v katalogu.

## <a name="publish-the-catalog"></a>Publikování katalogu
Publikování katalogu kontaktního střediska dokončíte informace o produktu v katalogu. Publikování také indikuje, že katalog je připraven k jakýmkoli dalším akcím, které chcete provést. Můžete například vytvořit tištěný katalog. Katalogy můžete publikovat ručně, nebo je můžete publikovat hromadně podle plánu. Před publikováním katalogu musí být katalog ověřený a schválený. Chcete-li změnit katalog po publikování, můžete katalog stáhnout a potom ho znovu publikovat.



