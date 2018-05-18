---
title: "Vylepšení POS pro serializované produkty"
description: "Toto téma uvádí seznam vylepšení, která byla provedena pro serializované produkty, abyste ušetřili čas a byli produktivnější."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 74a27761c065e475fa7c10c5812f0307df9f570e
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="pos-improvements-for-serialized-products"></a>Vylepšení POS pro serializované produkty

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Přehled 
Na základě nastavení v modulu Retail headquarters lze produkty klasifikovat jako serializované nebo neserializované. Když jsou produkty serializovány, každé položce lze přiřadit jedinečné číslo, které pomáhá sledovat záruky, sledovat položky a potvrdit vlastnictví. I když možnost poskytovat sériová čísla pro serializované produkty existovala již v našem moderním/cloudovém pokladním místě (POS), byla přidána některé vylepšení usnadňující pokladníkům ušetřit čas a být produktivnější.  

## <a name="pos-improvements"></a>Vylepšení POS

- **Sériová čísla nejsou požadována do doby přechodu k pokladně** – V předchozích verzích musel pokladník, který přidal serializovaný produkt k transakci, zadat sériové číslo. Tento požadavek se ve scénářích clientelingu ukázal problémovým, když pokladníci nebo zaměstnanci měli možnost návazného prodeje. Až do kroku zaplacení byly produkty v košíku často aktualizovány. Proto pokaždé, když pokladník přidal nový produkt, systém ho vyzval k zadání sériového čísla. Dialogové okno sériového čísla obsahuje nyní tlačítko **Přidat později**. Zaměstnanci obchodu tak mohou přidávat položku do transakce, ale zadat sériové číslo později. Zaměstnanci obchodu mohou rychle přidat a nahradit serializované položky do nákupního košíku a zadat pořadové číslo až před přechodem k pokladně. Není-li sériové číslo zadáno pro libovolný serializovaný produkt, pokladník, který se pokusí dokončit transakci, obdrží chybovou zprávu. Tato zpráva oznamuje, že pokladník musí zadat chybějící sériová čísla předtím, než bude pokračovat.

    Pro každou serializovanou položku, kde bylo sériové číslo přeskočeno, se zobrazí komentář pod řádkem transakce. Tento komentář oznamuje, že pro položku nebylo zadáno sériové číslo. Pokladník tedy může rychle vyhledat položky, kterým chybí sériového čísla.

    Nová operace **Přidat sériové číslo** také přidává sériové číslo k položkám, u kterých toto číslo chybí. Po zadání sériového čísla ho již nelze upravovat. Pokladník musí anulovat řádek a znovu přidat produkt. 
    
- **Sériová čísla nejsou povinná pro zadání objednávek odběratelů** – Objednávky odběratelů lze zadat do jednoho obchodu a provést jejich plnění z jiného obchodu. Pokladník, který zadává objednávku odběratele, nemusí zadat sériové číslo. Sériové číslo bude zadáno v průběhu kroku výdeje nebo vyskladnění. Sériové číslo však musí být zadáno pro všechny položky řádku, pro které je zvolen typ doručení **Provedení**. V opačném případě transakci nelze dokončit.    
- **Serializované produkty nejsou agregovány na obrazovce transakce** – Nastavení **Agregovat produkty** ve skupině polí **Terminál** na stránce **Funkční profil** umožňuje seskupovat stejné neserializované výrobky na obrazovce transakce. Při seskupení stejných produktů jsou lépe viditelné v mřížce transakcí. Nicméně vzhledem k tomu, že sériová čísla jsou zpravidla jedinečná a zaměstnanci obchodu nemusí zadávat sériová čísla až do okamžiku přechodu k pokladně, nastavení **Agregovat produkty** se nepoužívá pro serializované produkty. Proto serializované produkty nebude agregovány na obrazovce transakce, pokud zvolíte nastavení **Agregovat produkty**.
- **Možnosti vyhledávání v denících podle sériového čísla** – deníky lze nyní prohledávat podle sériových čísel. Otevřete operaci Deníky a stiskněte tlačítko Rozšířené vyhledávání na panelu aplikací. Pomocí tlačítka Přidat filtr lze použít filtr také na vyhledávání sériových čísel.

