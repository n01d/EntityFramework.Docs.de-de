---
title: Verwalten von Datenbankschemas – EF Core
author: bricelam
ms.date: 10/30/2017
ms.openlocfilehash: c1ebe33b5575cab76a54721ef86ecbcb7ff8b98b
ms.sourcegitcommit: dadee5905ada9ecdbae28363a682950383ce3e10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "42994384"
---
# <a name="managing-database-schemas"></a>Verwalten von Datenbankschemas
EF Core bietet zwei wesentliche Möglichkeiten, wie Sie Ihr EF Core-Modell und Ihr Datenbankschema synchron halten können. Um zwischen den beiden Optionen zu wählen, legen Sie fest, ob Ihr EF Core-Modell oder das Datenbankschema die einzige zuverlässige Datenquelle darstellt.

Wenn das EF Core-Modell die einzige zuverlässige Datenquelle darstellen soll, verwenden Sie [Migrationen][1]. Wenn Sie Änderungen an Ihrem EF Core-Modell vornehmen, werden bei dieser Vorgehensweise schrittweise die entsprechenden Schemaänderungen an Ihrer Datenbank vorgenommen, um die Kompatibilität mit Ihrem EF Core-Modell aufrechtzuerhalten.

Verwenden Sie [Reverse Engineering][2], wenn Ihr Datenbankschema die einzige zuverlässige Datenquelle sein soll. Diese Vorgehensweise ermöglicht es Ihnen, ein Gerüst für DbContext und die Entitätstypklassen durch Reverse Engineering Ihres Datenbankschemas in ein EF Core-Modell zu erstellen.

> [!NOTE]
> Die [APIs zum Erstellen und Löschen][3] können ebenfalls das Datenbankschema anhand Ihres EF Core-Modells erstellen. Diese werden jedoch in erster Linie für Tests, die Prototyperstellung und andere Szenarien eingesetzt, in denen die Datenbank gelegentlich gelöscht werden soll.


  [1]: migrations/index.md
  [2]: scaffolding.md
  [3]: ensure-created.md
