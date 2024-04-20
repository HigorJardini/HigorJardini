<a href="https://higorjardini.dev/"><img src="https://github.com/HigorJardini/HigorJardini/blob/main/higorjardini.dev.png?raw=true" alt="higorjardini.dev macbook image" min-width="300px" max-width="300px" width="300px" align="right"></a>

```js
import { Injectable } from '@higorjardini/common';
import { SoftwareEngineerDto } from './dto/software-enginner.dto';
import { Developer, DeveloperDocument } from './schemas/software-enginner.schemas';
import { Model } from 'mongoose';
import { InjectModel } from '@higorjardini/mongoose';

@Injectable()
export class SoftwareEngineerService {
  constructor(
    @InjectModel(Developer.name)
    private developerModel: Model<DeveloperDocument>,
  ) {}

  async create({ technologies }:  SoftwareEngineerDto) {
    const aboutMe = await this.findOne();
    if (!aboutMe) {
       const AboutMe = {
          name: "Higor Jardini",
          backend: true,
          portfolioLink: "https://higorjardini.dev/",
          skills: technologies
       }
    }
     return this.developerModel.create({ AboutMe });
  }

  async findOne() {
    return await this.developerModel.find().exec();
  }
}
```

##

![Snake animation](https://github.com/HigorJardini/Higorjardini/blob/output/github-contribution-grid-snake.svg)

