<p align="left">

  [![Linkedin: thaianebraga](https://img.shields.io/badge/-higorjardini-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/higorjardini/?locale=en_US)](https://www.linkedin.com/in/higorjardini/?locale=en_US)
  [![Twitter: ThaiiBraga](https://img.shields.io/twitter/follow/higor_jardini?style=social)](https://twitter.com/higor_jardini)
  [![GitHub Thaiane](https://img.shields.io/github/followers/HigorJardini?label=follow&style=social)](https://github.com/HigorJardini)

</p>

<a target="_blank" href="https://higorjardini.dev/"><img src="https://github.com/HigorJardini/HigorJardini/blob/main/higorjardini.dev.png?raw=true" alt="higorjardini.dev macbook image" min-width="300px" max-width="300px" width="300px" align="right"></a>

```js
// Hi, I'm Higor Jardini!
import { Injectable } from '@github/common';
import { SoftwareEngineerDto } from './dto/sf.dto';
import { Developer, DeveloperDocument } from './schemas/dev.schemas';
import { Model } from 'mongoose';
import { InjectModel } from '@github/mongoose';

@Injectable()
export class SoftwareEngineerService {
  constructor(
    @InjectModel(Developer.name)
    private developerModel: Model<DeveloperDocument>,
  ) {}

  async create({ skills }:  SoftwareEngineerDto) {
    const aboutMe = await this.findOne();
    if (!aboutMe) {
       const AboutMe = {
          name: "Higor Jardini",
          backend: true,
          frontend: null
          portfolioLink: "https://higorjardini.dev/",
          skills: skills
       }
       return this.developerModel.create({ AboutMe });
    }
  }

  async findOne() {
    return await this.developerModel.find().exec();
  }
}
```

##

![Snake animation](https://github.com/HigorJardini/Higorjardini/blob/output/github-contribution-grid-snake.svg)

